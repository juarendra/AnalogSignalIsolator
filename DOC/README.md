# Dokumentasi Analog Signal Isolator

Folder ini dipisahkan berdasarkan tujuan agar file yang dibutuhkan pengguna, teknisi, dan produksi tidak tercampur.

| Lokasi | Isi |
| --- | --- |
| [`USER_GUIDE/`](USER_GUIDE/) | Panduan pembeli/pengguna, halaman visual, foto PCB, dan pinout. |
| `00`–`05` | Diagram blok, skematik, pemilihan mode, dan pengkabelan Rev B2. |
| `06_BOM_and_Calculations_RevB2_LCSC.xlsx` | BOM, nilai komponen, dan perhitungan desain. |
| `07`–`08` | Aturan layout PCB serta pengujian/kalibrasi. |

Mulai dari [`USER_GUIDE/pinout-pcb.html`](USER_GUIDE/pinout-pcb.html) untuk pemasangan visual berdasarkan PCB fisik, atau [`USER_GUIDE/PINOUT_PCB_ID.md`](USER_GUIDE/PINOUT_PCB_ID.md) untuk versi Markdown.

## Catatan revisi

Foto PCB yang tersedia memperlihatkan pemilih mode berupa jumper solder `M2.4V1`, `M3.3V1`, dan `M5V1`. Dokumen teknik Rev B2 yang lebih lama menyebut `SW1` serta target 2,4/3,0/4,5 V. Selalu ikuti silkscreen dan BOM pada PCB yang benar-benar diterima, lalu lakukan kalibrasi dua titik.
