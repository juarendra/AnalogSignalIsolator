# BOM Terbaru — Skematik KiCad Saat Ini

File pembelian: [`09_BOM_Latest_Schematic_LCSC_Mouser.xlsx`](09_BOM_Latest_Schematic_LCSC_Mouser.xlsx). Versi teks untuk impor ke sistem pembelian: [`09_BOM_Latest_Schematic_LCSC_Mouser.csv`](09_BOM_Latest_Schematic_LCSC_Mouser.csv).

## Ruang lingkup dan sumber

- **Sumber desain:** `PCB/AnalogIsolator/AnalogIsolator/AnalogIsolator.kicad_sch` dan footprint dari PCB yang saat ini berada di *working tree*.
- **Tanggal pengecekan katalog:** 18 Juli 2026. Harga dan stok distributor berubah; cek kembali sebelum pemesanan.
- **Distributor:** kolom LCSC berisi nomor part LCSC untuk pembelian langsung. Kolom Mouser berisi nomor Mouser jika telah diverifikasi; jika yang diberikan hanya MPN, gunakan MPN itu untuk pencarian di Mouser dan verifikasi sebelum membeli.

## Hasil pencocokan skematik ↔ BOM

| Item | Hasil |
| --- | --- |
| Komponen pasif dan aktif | 24 baris BOM mencakup seluruh 33 referensi fisik pada PCB: C1–C10, D2, L1, M2.4V1/M3.3V1/M5V1, R1–R7/R9–R11, dan U1/U3/U4/U5/U7/U8/U9. |
| Pemilih mode | Skematik terbaru menggunakan tiga link 0 Ω (`M2.4V1`, `M3.3V1`, `M5V1`), bukan switch `SW1` pada BOM Rev B2 lama. Hanya **satu** link yang boleh dipasang. |
| Op-amp | Skematik terbaru memakai `U3 = OPA317IDBVR-TP` dan `U5 = OPA392DBVR`; BOM Rev B2 lama menyebut dua OPA317 dan tidak dapat dipakai apa adanya. |
| Footprint presisi | `R2` dan `R11` sekarang ber-footprint 0603. Jangan memakai resistor 0805 dari BOM lama tanpa revisi PCB. |

## Tindakan wajib sebelum rilis produksi

1. **D2 belum terdefinisi.** Skematik hanya memberi nilai `LED`; tentukan warna, intensitas, Vf, dan MPN. Jangan membuat PO untuk D2 sebelum data ini disetujui.
2. **U3 perlu keputusan sumber.** LCSC `C41431830` mengarah ke TECH PUBLIC, bukan TI. Untuk part TI resmi gunakan OPA317IDBVR dari Mouser (`595-OPA317IDBVR`) dan lakukan uji stabilitas loop.
3. **U4 dan U8/U9 tidak memiliki exact-match Mouser yang terverifikasi.** Sumber LCSC dapat digunakan; untuk substitusi Mouser, cek ukuran mekanik, pinout, regulasi, ripple, beban minimum, dan rating isolasi.
4. Jalankan ERC/DRC dan uji 0 V/5 V untuk setiap mode sebelum membekukan BOM sebagai revisi produksi.

## Referensi katalog yang diverifikasi

- [HCNR201-500E di LCSC](https://www.lcsc.com/product-detail/Phototransistors_AVAGO-Broadcom-HCNR201-500E_C27465.html) dan [Mouser](https://www.mouser.com/ProductDetail/Broadcom-Avago/HCNR201-500E)
- [OPA392DBVR di LCSC](https://www.lcsc.com/product-detail/Precision-Op-Amps_Texas-Instruments-OPA392DBVR_C3647166.html) dan [Mouser](https://www.mouser.com/ProductDetail/Texas-Instruments/OPA392DBVR)
- [IF0505S-1WR3 di LCSC](https://www.lcsc.com/product-detail/Isolated-Power-Modules_YLPTEC-IF0505S-1WR3_C5369637.html)
- [AO3401A di LCSC](https://www.lcsc.com/product-detail/MOSFETs_UMW-Youtai-Semiconductor-Co-Ltd-AO3401A_C347476.html)
- [BLM18AG601SN1D di LCSC](https://www.lcsc.com/product-detail/Ferrite-Beads_Murata-Electronics_C19330.html) dan [Mouser](https://www.mouser.com/en/ProductDetail/Murata-Electronics/BLM18AG601SN1D)
- [100 nF CL10B104KB8NNNC di LCSC](https://www.lcsc.com/product-detail/Multilayer-Ceramic-Capacitors-MLCC-SMD-SMT_Samsung-Electro-Mechanics-CL10B104KB8NNNC_C1591.html) dan [Mouser](https://www.mouser.com/ProductDetail/Samsung-Electro-Mechanics/CL10B104KB8NNNC)
