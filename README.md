# Linux Client Setup

Dieses Repository enthält eine **Umsetzungsanleitung** und ein **Bash-Skript** zur Umsetzung der BSI-Grundschutz-Bausteine  
[SYS.2.3 Clients unter Linux und Unix (Edition 2023)](https://www.bsi.bund.de/SharedDocs/Downloads/DE/BSI/Grundschutz/IT-GS-Kompendium_Einzel_PDFs_2023/07_SYS_IT_Systeme/SYS_2_3_Clients_unter_Linux_und_Unix_Edition_2023.pdf).

Ziel ist es, eine standardisierte, nachvollziehbare und überprüfbare Konfiguration für Linux-Clients der internen IT bereitzustellen.

---

## 📂 Projektstruktur

linux-client-setup/
├── docs/ # Umsetzungsanleitung (Markdown/PDF)
│ └── guide.md
├── scripts/ # Skripte zur Umsetzung
│ └── bsibase.sh
├── tests/ # Tests und Validierung
├── .github/workflows/ # GitHub Actions (CI)
│ └── test.yml
├── .gitignore
└── README.md

---

## ⚙️ Inhalte

- **docs/guide.md**  
  Enthält die schriftliche **Umsetzungsanleitung** mit allen Maßnahmen und Prüfschritten.

- **scripts/bsibase.sh**  
  Ein **Bash-Skript**, das zentrale Maßnahmen automatisiert:
  - Paketupdates & automatisches Patch-Management
  - SSH-Härtung (z. B. Passwort-Login deaktivieren, Root-Login verbieten)
  - Firewall (ufw) konfigurieren
  - Virenschutz & Rootkit-Scanner einrichten
  - Protokollierung mit auditd aktivieren
  - (Optional) Systemintegritätsprüfung mit AIDE

- **tests/**  
  Enthält optionale Prüfskripte, um die Konfiguration zu validieren.

---

## 🚀 Nutzung

### Voraussetzungen
- Linux-Distribution (getestet mit Ubuntu/Debian)
- `sudo`-Rechte
- Internetzugang für Updates

### Installation & Ausführung
1. Repository klonen:
   ```bash
   git clone https://github.com/ORG/bsi-linux-client-setup.git
   cd bsi-linux-client-setup/scripts
   ``
