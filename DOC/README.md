# Dokumentasi Analog Signal Isolator

Folder ini dipisahkan berdasarkan tujuan agar file yang dibutuhkan pengguna, teknisi, dan produksi tidak tercampur.

| Lokasi | Isi |
| --- | --- |
| [`USER_GUIDE/`](USER_GUIDE/) | Panduan pembeli/pengguna, halaman visual, foto PCB, dan pinout. |
| `00`–`05` | Diagram blok, skematik, pemilihan mode, dan pengkabelan Rev B2. |
| `06_BOM_and_Calculations_RevB2_LCSC.xlsx` | BOM, nilai komponen, dan perhitungan desain. |
| [`09_BOM_Latest_Schematic_LCSC_Mouser.xlsx`](09_BOM_Latest_Schematic_LCSC_Mouser.xlsx) | BOM baru hasil cocokkan dengan skematik saat ini; mencantumkan sumber LCSC dan Mouser serta item yang perlu disetujui. Lihat [catatan validasi](09_BOM_Latest_Schematic_LCSC_Mouser.md). |
| `07`–`08` | Aturan layout PCB serta pengujian/kalibrasi. |

Mulai dari [`USER_GUIDE/start-here.html`](USER_GUIDE/start-here.html) untuk pemasangan PCB fisik yang bertuliskan `AIN/AOUT`. Versi Markdown: [`USER_GUIDE/START_HERE_ID.md`](USER_GUIDE/START_HERE_ID.md). Referensi Rev B2 lama tetap tersedia untuk teknisi.

## Catatan revisi

Foto PCB yang tersedia memperlihatkan pemilih mode berupa jumper solder `M2.4V1`, `M3.3V1`, dan `M5V1`. Dokumen teknik Rev B2 yang lebih lama menyebut `SW1` serta target 2,4/3,0/4,5 V. Selalu ikuti silkscreen dan BOM pada PCB yang benar-benar diterima, lalu lakukan kalibrasi dua titik.
