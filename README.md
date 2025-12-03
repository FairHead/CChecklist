# 🚀 Embedded Learning Journey – Vom C-Basics zu Embedded Engineer

Dieses Repository dokumentiert meinen Weg vom „okay in C“ hin zu **solidem Embedded-Entwickler**, inkl.:

- Lern-Roadmap (C, Bare-Metal, RTOS, Kommunikation, Tooling, Linux/Yocto, Testing)
- Eigene Notizen, Code-Snippets und Mini-Experimente
- Übungsprojekte (z.B. GPIO-Treiber, RS-485-Tools, FreeRTOS-Demos, Network-Scanner)
- Materialsammlung (Links, PDFs, HTML-Checklisten, Skizzen, Schaltpläne)

Ziel: Am Ende bin ich **fit für Embedded-Job-Interviews** und habe einen sauberen, nachvollziehbaren Lernpfad + Portfolio-Projekte.

---

## 📂 Repo-Struktur (geplant)

> Hinweis: Ordner wachsen nach und nach, während ich lerne und Projekte baue.

```text
.
├─ README.md                         # Dieses Dokument
├─ docs/
│  ├─ embedded_roadmap_checkliste_v2.html   # Interaktive Roadmap-Checkliste (lokal im Browser nutzbar)
│  └─ notes/                        # Eigene Notizen (Markdown, PDFs, Skizzen)
├─ c-basics/
│  ├─ exercises/                    # Kleine C-Übungen (Pointer, Structs, Speicher, Modulstruktur etc.)
│  └─ examples/                     # Beispielcode nach Themen
├─ bare-metal/
│  ├─ blink/                        # Bare-Metal Blink + GPIO-Treiber
│  ├─ timer-interrupts/             # Timer + Interrupts
│  └─ linker-startup/               # Startup-Code, Vector Table, Linker-Skripte
├─ drivers/
│  ├─ gpio/                         # Eigene GPIO-HAL / Treiber
│  ├─ uart-rs485/                   # UART/RS-485-Treiber & Protokoll-Beispiele
│  └─ i2c-spi/                      # I²C / SPI-Treiber, PCF8574 etc.
├─ freertos/
│  ├─ tasks-queues/                 # Tasks, Queues, Mutex, Semaphores
│  └─ examples/                     # Kleine Demos (Producer/Consumer, Periodic Tasks)
├─ networking/
│  ├─ mdns-scanner/                 # mDNS / TCP/UDP-Device-Scanner
│  └─ rest-client/                  # Simple REST/HTTP-Client auf Embedded-Basis
├─ linux-yocto/
│  ├─ notes/                        # Notizen zu Device Tree, Treibern, Yocto
│  └─ examples/                     # Kleine Experimente
├─ testing/
│  ├─ unity-examples/               # Unit Tests mit Unity Test Framework
│  └─ ci-experiments/               # (später) CI-Setup für Tests
└─ portfolio/
   ├─ relay-adc-monitor/            # Projekt: Relay + ADC Board Monitor
   ├─ rs485-sniffer/                # Projekt: RS-485 Bus Sniffer + CRC Validate
   ├─ freertos-system/              # Projekt: FreeRTOS Task System mit IPC
   └─ mini-bootloader/              # Projekt: Mini-Bootloader-Konzept
```

---

## 🧱 Lern-Roadmap (Übersicht)

Die vollständige Roadmap steckt in:

- `docs/embedded_roadmap_checkliste_v2.html`

Darin sind enthalten:

- **C & Embedded C (erweitert)**  
  Syntax, Pointer, Speicher, Modularisierung, Datenstrukturen, MISRA-C, Best Practices
- **Mikrocontroller & Bare Metal**  
  Register, Interrupts, Startup-Code, Linker, Bare-Metal-Blink & Treiber
- **Hardware & Elektronik-Basics**  
  Spannungsteiler, MOSFET, Relais, RS-485, I²C, SPI, Messtechnik, Oszilloskop
- **RTOS / FreeRTOS**  
  Tasks, Queues, Semaphores, Mutex, Prioritäten, Race Conditions
- **Kommunikation & Networking**  
  UART, RS-485, I²C/SPI, TCP/UDP, mDNS, REST/API
- **Tooling**  
  VS Code + ESP-IDF, CMake, Debugging (JTAG/SWD, gdb, OpenOCD)
- **Embedded Linux & Yocto**  
  Device Tree, Kernel-Module, Yocto Layers & Recipes
- **Testing & Code-Qualität**  
  Unit-Tests (Unity), Clean Code, Architektur & Struktur
- **Exkursionen**  
  Türantriebe, Bootloader & Flash, Oszilloskop, Embedded Security

In der HTML-Datei gibt es Checkboxen, mit denen ich meinen Fortschritt tracke (werden im Browser lokal gespeichert).

---

## ✅ Wie ich dieses Repo nutze

Dieses Repository ist mein persönliches **Lern- und Projekt-Workspace**:

- 📘 **Theorie & Notizen**  
  In `docs/notes/` landen Zusammenfassungen, Zeichnungen, kleine Erklärungen (Markdown, PDFs).

- 💻 **Übungscode & Experimente**  
  In den jeweiligen Themenordnern (`c-basics/`, `bare-metal/`, `drivers/`, …) landet alles, was ich beim Lernen codiere.

- 🧪 **Testing & Qualität**  
  In `testing/` baue ich Unit-Tests, z.B. mit Unity Test Framework, und spiele mit Test-Strukturen und später eventuell CI.

- 🧩 **Portfolio-Projekte**  
  In `portfolio/` landen bewusst sauber strukturierte Projekte, die ich im Lebenslauf / GitHub-Profil zeigen kann.

---

## 🧰 Tools & Umgebung

Typische Umgebung (kann sich im Laufe des Lernens weiterentwickeln):

- **IDE / Editor**
  - Visual Studio Code
  - ggf. CLion / VS / andere, je nach Projekt
- **Toolchains**
  - `gcc`, `clang`
  - ESP-IDF Toolchain
  - ggf. ARM GCC für STM32
- **Debugging**
  - `gdb`, `OpenOCD`
  - JTAG/SWD Debugger (z.B. J-Link, ST-Link)
- **Testing**
  - Unity Test Framework (C)

---

## 🧪 Lern- & Aufgaben-Tracking

Grundidee: Alles, was ich im Lernprozess mache, hat einen sichtbaren Platz im Repo.

- [ ] C-Basics durchgehen und erste Übungen in `c-basics/exercises/` ablegen  
- [ ] Pointer & Speicher-Deep-Dive, kleine Demos in `c-basics/examples/`  
- [ ] Erstes Bare-Metal-Blink-Projekt unter `bare-metal/blink/`  
- [ ] Eigenen GPIO-Treiber schreiben (`drivers/gpio/`)  
- [ ] RS-485 Sniffer & Protokoll-Auswertung (`drivers/uart-rs485/`, `portfolio/rs485-sniffer/`)  
- [ ] FreeRTOS-Demos & Tasks (`freertos/`)  
- [ ] Network-Scanner mit mDNS/TCP/UDP (`networking/mdns-scanner/`)  
- [ ] Mini-Bootloader-Konzept in `portfolio/mini-bootloader/` dokumentieren  
- [ ] Unit-Tests mit Unity (`testing/unity-examples/`)  

Die HTML-Roadmap in `docs/embedded_roadmap_checkliste_v2.html` ergänzt das Ganze mit sehr detaillierten Unterpunkten, Tutorials & Interviewfragen.

---

## 🎯 Ziel

Am Ende dieses Repos möchte ich:

- Einen **klaren roten Faden** von C-Grundlagen bis hin zu professionellen Embedded-Themen haben.
- Mehrere **vorzeigbare Projekte** besitzen, die Embedded-Firmen nachvollziehen können:
  - Sauberer C-Code
  - Umgang mit RTOS, Kommunikation, Treibern, Debugging
  - Verständnis von Hardware & Schaltplänen
- Gut vorbereitet in **Embedded-Jobinterviews** sitzen, mit:
  - Soliden Fachfragen-Antworten (siehe Roadmap/HTML)
  - Konkreten, vorzeigbaren Projekten in diesem Repo

---

## 🔒 Lizenz / Nutzung

Dieses Repo ist in erster Linie mein persönlicher Lernpfad.  
Lizenz: *(hier kannst du z.B. MIT, Apache 2.0 oder „All Rights Reserved“ eintragen – je nachdem, ob andere deinen Code nutzen dürfen oder nicht).*  
