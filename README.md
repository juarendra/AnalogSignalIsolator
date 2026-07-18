# Analog Signal Isolator

Modul isolator sinyal analog 0–5 V untuk MCU dan PLC, dengan keluaran yang dapat disesuaikan untuk kelas ADC 2,4 V, 3,3 V, atau 5 V.

## Mulai di sini

- [Panduan pinout visual (buka di browser)](DOC/USER_GUIDE/pinout-pcb.html)
- [Panduan pinout Markdown](DOC/USER_GUIDE/PINOUT_PCB_ID.md)
- [Panduan pengguna visual (buka di browser)](DOC/USER_GUIDE/panduan-visual.html)
- [Indeks dokumentasi teknis dan produksi](DOC/README.md)

## Struktur proyek

| Folder | Isi |
| --- | --- |
| `DOC/` | Dokumentasi pengguna, skematik, BOM, pengujian, dan referensi produksi. |
| `PCB/AnalogIsolator/AnalogIsolator/` | Proyek KiCad, library lokal, dan berkas Gerber/drill produksi. |

> Gunakan catu host 5 V yang teratur dan dibatasi arus. Jangan menyatukan ground sisi MCU dengan ground sisi sensor.
