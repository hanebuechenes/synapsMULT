# synapsMULT — Buffered Multiple with Input Level LEDs

`synapsMULT` ist ein 4-Kanal Eurorack-Verteiler (Buffered Multiple) im Open-Source-Hardware-Format. Es verarbeitet sowohl Audio- als auch Steuerspannungssignale (CV) präzise und verlustfrei. 

Dank der internen Kaskadierung (Daisy-Chaining) lässt sich das Modul extrem flexibel als 1-zu-12, zweimal 1-zu-6 oder viermal 1-zu-3 Mult nutzen. Integrierte bipolare LEDs an jedem Kanal bieten eine direkte visuelle Pegelanzeige.

---

## Key Features

* **4 Unabhängige Buffer:** Basierend auf dem op-amp Klassiker TL074.
* **1-to-12 Normalisierung:** Kaskadierte Klinkenbuchsen schalten das Signal automatisch von `IN1` auf alle Kanäle durch, solange keine weiteren Eingänge belegt sind.
* **Visual Level Indication:** Bipolare LEDs (Rot/Grün) pro Eingang zeigen Signalpegel, Polarität (CV) und Dynamik (Audio) in Echtzeit an.
* **Saubere Entkopplung:** $1\text{k}\Omega$ Schutzwiderstände an allen Ausgängen zur Impedanzanpassung und Schutz vor Kurzschlüssen.
* **Low Component Count:** Einfach aufzubauen, ideal für DIY-Einsteiger und präzise genug für Pitch-CV.

---

## Module Overview

| Kanal | Eingang | Normalisiert von | Ausgänge | Status-LED |
| :--- | :--- | :--- | :--- | :--- |
| **Kanal 1** | IN1 | — | OUT1, OUT2, OUT3 | D3 |
| **Kanal 2** | IN2 | IN1 | OUT1, OUT2, OUT3 | D4 |
| **Kanal 3** | IN3 | IN2 | OUT1, OUT2, OUT3 | D5 |
| **Kanal 4** | IN4 | IN3 | OUT1, OUT2, OUT3 | D6 |

---

## Technical Specifications

* **Format:** Eurorack Modul
* **Versorgungsspannung:** $\pm12\text{V}$ (Standard Eurorack Power Ribbon Connector)
* **Op-Amp:** 1x TL074 Quad Operational Amplifier
* **LED-Vorwiderstände:** $3.3\text{k}\Omega$ für bipolare LEDs
* **Ausgangswiderstände:** $1\text{k}\Omega$ (Metallschicht 1%)

---

## Project Structure

```text
.
├── hardware/            # KiCad Schaltplan & PCB-Layout (.kicad_sch, .kicad_pcb)
├── gerbers/             # Produktionsdateien für PCB-Fertigung (JLCPCB ready)
├── docs/                # Bestückungsplan, BOM & Grafiken
├── LICENSE              # Lizenzdateien
└── README.md            # Projekt-Dokumentation



## License

Dieses Projekt ist unter den folgenden Open-Source-Lizenzen veröffentlicht:

    Hardware (Schaltplan & Layout): CERN OHL-P-2.0 (CERN Open Hardware Licence Permissive)

    Dokumentation: MIT License
