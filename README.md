# Analog Signal Isolator

> Isolator sinyal analog 0–5 V untuk menghubungkan sensor ke ESP32, Arduino, MCU, atau PLC tanpa menyatukan ground kedua sisi.

<p align="center">
  <img src="DOC/USER_GUIDE/assets/pcb-top-view.jpg" alt="PCB Analog Signal Isolator — tampak atas" width="760">
</p>

<p align="center">
  <a href="DOC/USER_GUIDE/pinout-pcb.html"><strong>Lihat pinout visual &rarr;</strong></a>
  &nbsp;·&nbsp;
  <a href="DOC/USER_GUIDE/assets/pinout-pcb-infographic.png"><strong>Unduh gambar pinout &rarr;</strong></a>
</p>

## Kenapa menggunakan modul ini?

- **Isolasi galvanik** antara sisi sensor dan sisi MCU/PLC untuk membantu mengurangi *ground loop* dan gangguan.
- **Input sensor 0–5 V DC** dengan keluaran analog terisolasi `AOUT`.
- **Catu sensor 5 V terisolasi** tersedia langsung pada konektor sisi sensor.
- **Mode untuk kelas ADC 2,4 V / 3,3 V / 5 V** melalui satu jumper pilihan (`FIT ONE ONLY`).
- **Siap untuk dokumentasi dan produksi:** proyek KiCad, Gerber, BOM, skematik, serta prosedur pengujian tersedia di repositori.

## Gambaran koneksi

| MCU SIDE | SENSOR SIDE |
| --- | --- |
| `5V` — catu masuk modul | `5V` — catu keluar terisolasi untuk sensor |
| `GND` — ground MCU/PLC | `GND` — ground sensor terisolasi |
| `AOUT` — ke input ADC | `AIN` — dari output sensor 0–5 V |

> [!CAUTION]
> **Jangan hubungkan ground MCU ke ground sensor.** Kedua sisi harus tetap terpisah agar isolasi bekerja.

## Mulai cepat

1. Saat daya mati, pilih **satu** jumper mode: `M2.4V1`, `M3.3V1`, atau `M5V1`.
2. Hubungkan sensor 0–5 V ke `AIN` dan `GND` pada **SENSOR SIDE**.
3. Hubungkan ADC ke `AOUT`, catu +5 V ke `5V`, dan ground host ke `GND` pada **MCU SIDE**.
4. Nyalakan catu 5 V yang teratur dan memiliki pembatas arus, kemudian kalibrasikan pembacaan 0 V dan 5 V.

## Dokumentasi

| Dokumen | Kegunaan |
| --- | --- |
| [Pinout visual](DOC/USER_GUIDE/pinout-pcb.html) | Cara pemasangan dari foto PCB atas/bawah; buka di browser. |
| [Gambar pinout siap dibagikan](DOC/USER_GUIDE/assets/pinout-pcb-infographic.png) | Infografik untuk pembeli, marketplace, atau teknisi lapangan. |
| [Panduan pengguna](DOC/USER_GUIDE/panduan-visual.html) | Penjelasan kerja, mode, wiring, kalibrasi, dan troubleshooting. |
| [Indeks dokumen teknis](DOC/README.md) | Skematik, BOM, aturan PCB, dan prosedur pengujian. |

## Struktur proyek

| Folder | Isi |
| --- | --- |
| `DOC/USER_GUIDE/` | Panduan pembeli, pinout, gambar produk, dan aset visual. |
| `DOC/` | Skematik, BOM, pengujian, serta referensi teknis Rev B2. |
| `PCB/AnalogIsolator/AnalogIsolator/` | Proyek KiCad, library lokal, Gerber, dan drill file produksi. |

> Rev B2 tidak memasang TVS dan sekering resettable (PPTC) pada papan. Untuk pemasangan yang andal, gunakan catu host 5 V yang teratur, dibatasi arus, dan perlindungan surge pada level sistem bila diperlukan.
