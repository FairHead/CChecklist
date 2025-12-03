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
