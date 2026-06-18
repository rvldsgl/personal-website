---
title: "Rupiah Rp18.000: Orang Indonesia Panik Tidak?"
description: "Ekonom mengukur dampak rupiah melemah lewat inflasi dan data perdagangan. Saya mengukurnya lewat apa yang orang Indonesia cari di Google. Hasilnya cukup mengejutkan."
date: 2026-06-18
tags: ["data", "indonesia", "economics"]
draft: false
---

Awal Juni 2026, rupiah tembus angka yang belum pernah terjadi sebelumnya: **Rp18.190 per dolar**.

Bukan rekor biasa. Ini level terendah dalam sejarah modern Indonesia.

Saya tinggal di sini. Saya merasakannya. Dan saya penasaran dengan satu pertanyaan yang tidak bisa dijawab oleh Bloomberg atau Bank Indonesia:

*Apa yang orang Indonesia sebenarnya lakukan saat rupiah jatuh?*

Bukan apa yang kata ekonom. Bukan proyeksi kebijakan moneter. Tapi tindakan nyata orang-orang biasa — yang bisa kita baca lewat apa yang mereka cari di Google.

---

## Caranya

Saya ambil dua sumber data:

**1. Kurs USD/IDR** — dari Yahoo Finance, harian, Januari sampai Juni 2026.

**2. Google Trends** — data pencarian mingguan dari Indonesia, untuk beberapa kata kunci:
- `beli dolar` — panik beli dolar?
- `kurs dollar` — cek kurs (versi finance-minded)
- `kurs rupiah` — cek kurs (versi orang biasa)
- `dollar naik` — sadar dolar lagi naik
- `inflasi` — khawatir inflasi
- `resesi` — takut resesi

Lalu saya plot keduanya dan lihat apa yang terjadi.

---

## Gambaran Besarnya

Ini adalah perjalanan rupiah dari awal tahun:

![USD/IDR exchange rate January to June 2026 — showing the steady rise from Rp 16,668 to the historic peak of Rp 18,190 on June 9](/images/rupiah/01_overview.png)

Awal Januari: Rp16.668. Cukup normal.

Lalu rupiah mulai melemah perlahan dari Februari. Lompat lebih cepat dari Mei. Lalu tiba-tiba — dalam dua minggu terakhir Mei dan awal Juni — jatuh tajam menembus 18.000.

Katalis utamanya: ketegangan geopolitik di Timur Tengah mendorong harga minyak naik. Indonesia sebagai net importer minyak butuh lebih banyak dolar untuk bayar impor energi. Surplus perdagangan menyempit. Rupiah kehabisan buffer. Tembus Rp18.000.

Sekarang pertanyaannya: apa yang terjadi di sisi perilaku manusia?

---

## Temuannya

### "Beli dolar" meledak — seminggu sebelum rupiah menyentuh bottom

Ini yang paling menarik:

![Dual-axis chart: USD/IDR rate (red, daily) vs beli dolar Google searches (blue dashed, weekly). Searches peaked May 31 — 9 days before the rate peaked on June 9.](/images/rupiah/02_beli_dolar_vs_rate.png)

Pencarian `beli dolar` mencapai puncaknya di **31 Mei** — sementara rupiah baru menyentuh level terburuknya pada **9 Juni**.

Artinya orang sudah panik beli dolar **sebelum** rupiah benar-benar jatuh ke titik terdalam.

Ini menarik karena menunjukkan dua hal:
1. Publik sudah bisa "membaca" arah pergerakan dari berita-berita sebelumnya
2. *Pencarian Google bisa jadi leading indicator* — sinyal yang muncul sebelum data ekonomi resmi rilis

Korelasi `beli dolar` dengan kurs: **r = +0.805**. Sangat kuat.

---

### Panel lengkap semua kata kunci

Ini gambaran seluruh kata kunci yang saya track:

![Panel chart showing all 6 search terms against the exchange rate. beli dolar, kurs dollar, dollar naik, and kurs rupiah all spiked in May-June. Resesi peaked in January and didn't spike with the crash.](/images/rupiah/03_all_terms_panel.png)

Beberapa hal yang menonjol:

**Yang spiked bersamaan dengan rupiah:**
- `beli dolar` — r = +0.805
- `kurs dollar` — r = +0.903 (tertinggi)
- `kurs rupiah` — r = +0.903 (sama kuatnya)
- `dollar naik` — r = +0.794

**Yang tidak bergerak seperti yang diharapkan:**
- `resesi` — peaknya di **Januari**. Saat rupiah benar-benar jatuh di Mei-Juni, pencarian *resesi* justru relatif flat. Orang lebih khawatir soal resesi di awal tahun dibanding saat krisis kurs yang sebenarnya.
- `inflasi` — r = +0.362. Ada korelasi, tapi lemah. Orang tidak langsung connect "rupiah lemah = inflasi."

---

## Interpretasi

Kalau kita baca data ini, ada cerita yang cukup jelas:

Orang Indonesia yang aktif merespons krisis rupiah ini adalah orang-orang yang **langsung cari cara proteksi** — beli dolar, cek kurs. Bukan yang mikir panjang soal resesi atau inflasi.

Yang menarik: `kurs dollar` dan `kurs rupiah` punya korelasi tertinggi (+0.903 keduanya). Ini masuk akal — saat kurs bergerak ekstrem, orang langsung buka Google dan ketik "kurs rupiah berapa sekarang." Itu refleks, bukan analisis.

Sebaliknya, `resesi` yang justru peak di Januari bisa berarti: di awal tahun ada banyak wacana resesi global (tarif Trump, slowdown ekonomi), tapi saat krisis kurs aktual terjadi di Mei-Juni, orang sudah tidak fokus ke narasi itu — mereka fokus ke angka di layar HP.

---

## Caveats

Saya harus jujur tentang keterbatasan ini:

**Google Trends hanya mengukur orang yang Google.** Bukan semua orang yang khawatir rupiah itu langsung buka Google. Banyak yang langsung telepon keluarga, WhatsApp grup arisan, atau diam-diam beli emas tanpa search apa pun.

**Data mingguan itu kasar.** Google Trends memberikan data per minggu untuk range ini, bukan harian. Jadi timing "peak May 31" sebenarnya berarti "puncaknya di minggu yang dimulai 31 Mei" — bisa jadi actual peak-nya di hari lain dalam minggu itu.

**Korelasi bukan kausalitas.** Ini sudah klise, tapi tetap relevan. Rupiah melemah dan orang search `beli dolar` bisa jadi keduanya respons dari hal ketiga (berita yang sama), bukan satu yang menyebabkan yang lain.

---

## Kesimpulan

Ketika rupiah tembus Rp18.000 untuk pertama kalinya dalam sejarah modern, orang Indonesia meresponsnya dengan cara yang bisa diprediksi tapi tetap menarik untuk dikonfirmasi:

Mereka cek kurs. Mereka cari cara beli dolar. Dan — ini yang saya rasa paling menarik — mereka melakukan ini **sebelum** kurs menyentuh titik terburuknya.

Bukan ketakutan pasif. Ada antisipasi aktif.

Apakah itu membuat situasinya lebih baik atau lebih buruk? Itu pertanyaan untuk ekonom lain. Saya cuma orang yang iseng download data sambil nungguin rupiah balik ke 16.000.

*(Spoiler: belum balik.)*

---

*Data: exchange rate dari Yahoo Finance, Google Trends data via Google Trends. Analisis dan visualisasi menggunakan Python. Kode lengkap di [GitHub](https://github.com/rvldsgl).*
