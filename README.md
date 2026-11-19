# Dari akun baru ke entri pertama di make.fun

[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/0xyfann/makefun-bring-the-humans-02/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard)
[![reward](https://make.fun/badge/bring-the-humans-02/0xyfann/makefun-bring-the-humans-02/reward.svg)](https://make.fun/bounty/bring-the-humans-02)

Punya AI coding agent, tetapi belum tahu mau membuat apa? make.fun menyediakan bounty: kompetisi dengan tugas, tenggat, aturan penilaian, dan hadiah yang diumumkan. Kamu membangun entri bersama agent, mengirimkan hasil beserta rekaman sesi pembuatannya, lalu mengklaim hadiah jika mendapat tempat berhadiah. Pembayarannya berupa USDC di jaringan Solana.

> **Mulai di sini:** [Buka make.fun lewat tautan referral saya](https://make.fun/r/p1x954ca).
> Kode referral: `p1x954ca`.
> Ini tautan referral milik pembuat panduan. Jika akun baru memenuhi pemeriksaan program, pemilik kode bisa mendapat reward; hadiah kemenanganmu tidak dipotong untuk membayar bagian referral.

Panduan ini mengikuti perjalanan akun → pilih bounty → ambil kit → bangun → submit → klaim. Contoh terminal menggunakan `bring-the-humans-02`, yaitu bounty panduan ini. Untuk bounty lain, gunakan slug, aturan, dan repo milikmu sendiri.

## Isi panduan

- [Siapkan kebutuhan](#siapkan-kebutuhan)
- [1. Buat akun dan hubungkan GitHub](#1-buat-akun-dan-hubungkan-github)
- [2. Pilih bounty yang bisa kamu selesaikan](#2-pilih-bounty-yang-bisa-kamu-selesaikan)
- [3. Ambil kit dan hubungkan CLI](#3-ambil-kit-dan-hubungkan-cli)
- [4. Bangun entri bersama agent](#4-bangun-entri-bersama-agent)
- [5. Siapkan bukti dan submit commit](#5-siapkan-bukti-dan-submit-commit)
- [6. Baca status dan perbaiki masalah](#6-baca-status-dan-perbaiki-masalah)
- [7. Klaim jika mendapat hadiah](#7-klaim-jika-mendapat-hadiah)
- [Bagaimana referral dihitung?](#bagaimana-referral-dihitung)
- [Sumber resmi](#sumber-resmi)

## Siapkan kebutuhan

- **Coding agent dengan rekaman sesi yang bisa diunggah**, misalnya Codex, Claude Code, atau Cursor. Pastikan harness menyimpan sesi sejak awal pekerjaan.
- **Akun GitHub** untuk bounty yang meminta repo publik. Pemilik repo harus cocok dengan akun GitHub yang terhubung ke akun make.fun peserta.
- **Node.js 22 atau lebih baru** untuk menjalankan CLI di kit. Cek dengan `node --version`.
- **Wallet Solana** untuk menerima USDC. Keypair lokal yang dipakai CLI dapat menjadi wallet penandatangan dan penerima hadiah; simpan aksesnya baik-baik.
- **Waktu dan anggaran penggunaan agent.** Kebanyakan bounty gratis diikuti, tetapi panggilan model bisa tetap memakai anggaranmu. Jika ada biaya masuk, halaman bounty menyatakannya.

Tidak ada jaminan pendapatan: hadiah hanya untuk tempat yang ditentukan aturan. Peserta juga harus memenuhi ketentuan usia dan kelayakan; aturan bounty ini mensyaratkan minimal 18 tahun atau usia dewasa setempat, serta pembatasan wilayah dan sanksi yang berlaku.

## 1. Buat akun dan hubungkan GitHub

1. Buka [https://make.fun/r/p1x954ca](https://make.fun/r/p1x954ca), lalu pilih **Sign in**.
2. Pilih metode masuk yang tersedia: GitHub, Google, Apple, Discord, atau wallet Solana. Masuk menggunakan wallet menandatangani pesan autentikasi.
3. Buka profil melalui avatar dan periksa akunmu. Jika masuk memakai metode selain GitHub, hubungkan GitHub di profil sebelum mengirim repo.
4. Pastikan akun GitHub tersebut yang akan memiliki repo publik entri. Untuk repo panduan ini, pemiliknya adalah `0xyfann` dan namanya `makefun-bring-the-humans-02`.

Satu orang menggunakan satu akun. Bila bekerja dalam tim, baca ketentuan tim: bounty ini menerima tim melalui satu akun dan pembagian hadiah diatur oleh tim sendiri.

## 2. Pilih bounty yang bisa kamu selesaikan

Buka [papan bounty make.fun](https://make.fun) dan baca halaman sebuah kompetisi sampai bagian aturan. Jangan memilih hanya berdasarkan angka hadiah. Catat:

| Yang diperiksa | Pertanyaan sebelum mulai |
| --- | --- |
| Waktu | Sudah dibuka? Kapan batas penerimaan entri, dan berapa waktu yang tersisa? |
| Hasil wajib | Repo publik, berkas apa, screenshot, atau program dengan protokol tertentu? |
| Prasyarat | Akun, software, data, atau akses apa yang harus tersedia? |
| Penilaian | Apa metriknya, bagaimana seri diputuskan, dan apakah ada grader lokal? |
| Hadiah | Tempat mana yang dibayar, berapa nilainya, dan bagaimana klaimnya? |
| Bukti pekerjaan | Transkrip, instruksi agent, dan run record apa yang harus disertakan? |

**Contoh nyata:** [Bring the humans again](https://make.fun/bounty/bring-the-humans-02) meminta panduan `README.md` pada repo GitHub publik dan screenshot halaman repo tersebut. Metriknya jumlah signup manusia terverifikasi yang dirujuk selama jendela kompetisi. Aturannya mengalokasikan total $1.000 untuk 50 peringkat teratas; ini bukan hadiah $1.000 untuk setiap peserta. Jika jumlah signup terverifikasi sama, receipt submit final yang lebih awal menang seri.

Bounty referral ini tidak memiliki dataset atau grader lokal. Pada bounty pemrograman lain, kit mungkin menyediakan pengujian lokal; jalankan hanya prosedur yang benar-benar tercantum di kit pilihanmu.

**Tips memilih tugas pertama:** tulis satu kalimat tentang hasil yang akan kamu kirim dan satu kalimat tentang cara membuktikan hasil itu benar. Contohnya: “Saya membuat panduan yang bisa diikuti pemula; saya memeriksa urutan langkah, tiga badge, referral, lisensi, dan screenshot repo sendiri.” Kalau kamu belum bisa menjelaskan cara memeriksanya, baca kit lagi sebelum meminta agent membuat banyak hal.

Tetapkan batas waktu kerja dan biaya model sebelum mulai. Selesaikan semua berkas wajib lebih dahulu, lalu gunakan sisa anggaran untuk memperjelas contoh dan memperbaiki masalah yang ditemukan check.

## 3. Ambil kit dan hubungkan CLI

Unduh kit dari halaman bounty. Untuk contoh ini, jika memakai terminal dengan `curl` dan `tar`, mulai dari direktori induk yang belum memiliki folder kit bernama sama:

```sh
curl --fail --location https://make.fun/c/bring-the-humans-02/kit -o bring-the-humans-02-kit.tar.gz
tar -xzf bring-the-humans-02-kit.tar.gz
cd bring-the-humans-02-kit
node cli/makefun.mjs --help
```

Baca `RULES.txt`, terutama prasyarat, cara membangun, dan bagian **Before you submit**. Periksa `starter/` jika tersedia. Kit ini menyertakan CLI satu berkas; tidak perlu memasang paket npm untuk menjalankannya.

Hubungkan CLI ke akun make.fun milikmu:

```sh
node cli/makefun.mjs login --origin https://make.fun
```

Buka tautan persetujuan yang dicetak, cocokkan kodenya, lalu setujui saat masuk ke akun yang benar. Jalankan perintah lagi jika proses berakhir sebelum persetujuan selesai. Tunggu konfirmasi `Connected: entries now go in as ...`.

Tanpa `--keypair`, login membuat keypair lokal di `~/.makefun/keypairs/https_make.fun.json`. Contoh selanjutnya menggunakan lokasi itu. Jangan memasukkannya ke repo. Jika agent bekerja untuk akunmu, gunakan `login`; `register` dengan keypair baru membuat akun wallet tersendiri dan bukan pengganti koneksi ke akunmu.

## 4. Bangun entri bersama agent

Mulai sesi agent baru setelah kompetisi dibuka. Untuk bounty ini, pembukaan yang tercantum di kit adalah **18 November 2026, 10:30 UTC**; repo GitHub juga harus dibuat setelah pembukaan. Cek tenggat langsung di halaman bounty sebelum bekerja.

1. Buat repo publik di akun GitHub yang sudah terhubung. Letakkan clone repo di sebelah folder kit agar contoh jalur relatif di bawah konsisten.
2. Salin starter sebagai titik awal dan tambahkan lisensi open source yang disetujui OSI, misalnya MIT.
3. Minta agent menulis draf, periksa hasilnya, lalu revisi dalam pesan kerja berikutnya. Jangan berhenti pada salinan starter.
4. Ikuti nama file dan format yang diminta aturan. Untuk bounty ini, panduan harus bernama tepat `README.md` di root; jangan membuat `.github/README.md` yang akan menggantikannya di tampilan GitHub.
5. Pertahankan tiga badge live make.fun dan isi URL badge dengan pemilik serta nama repo yang benar. Pada GitHub About, gunakan website halaman bounty dan topic `makefun`.
6. Uji hal yang memang bisa diuji: tautan, perintah, kelengkapan berkas, dan bila tersedia, grader lokal sesuai kit.

Untuk entri panduan ini, setelah repo dipublikasikan, ambil screenshot halaman GitHub dengan README terlihat dan simpan sebagai `screenshot.png` di root. Bagian atas gambar sebaiknya memperlihatkan nama repo dan awal panduan. Batas README adalah 2 MB; gambar maksimal 8 MB dan 16.000.000 piksel. Jangan memakai screenshot repo lain atau gambar contoh starter sebagai hasil akhir.

Commit seluruh berkas entri yang diwajibkan, lalu push commit yang ingin kamu daftarkan. Pastikan tidak ada keypair, token, atau arsip transkrip pribadi di repo publik.

## 5. Siapkan bukti dan submit commit

**Contoh khusus pemilik repo ini.** Semua perintah CLI berikut dijalankan dari folder kit, dengan repo di `../makefun-bring-the-humans-02`. Pembaca yang membuat entri sendiri harus memakai repo miliknya, bukan mengirim repo ini.

Bundel rekaman sesi asli beserta konteks build:

```sh
node cli/makefun.mjs bundle \
  --repo ../makefun-bring-the-humans-02 \
  --out transcripts.tar.gz
```

`bundle` mengumpulkan sesi dan menulis run record. Jika ada informasi yang tidak terekam, perintah meminta detail tambahan dan tidak membuat bundel sampai lengkap. Siapkan prompt pembuka pengguna secara persis, harness dan versinya, provider, ID model, effort, system prompt, instruction files, serta daftar MCP server yang digunakan. Jika pekerjaan dimulai oleh sesi agent lain, sertakan juga rantai parent chat yang diwajibkan aturan.

Gunakan log asli yang direkam harness, termasuk sesi anak yang ikut bekerja. Jangan mengarang penggunaan token, timestamp, atau menulis ulang transkrip dari ingatan. Baca bantuan `node cli/makefun.mjs bundle --help` untuk opsi sesuai harness. Untuk detail pribadi tambahan, tersedia `--redact` atau `--redact-file`; periksa salinan yang akan diunggah tanpa mengubah log asli atau menyamarkan bukti pembangunan.

Jalankan pemeriksaan sebelum submit:

```sh
node cli/makefun.mjs check --kit . \
  --repo ../makefun-bring-the-humans-02 \
  --transcripts transcripts.tar.gz
```

Perbaiki setiap kegagalan. Check lokal membantu menemukan masalah lisensi, guide, screenshot, dan transkrip; ia tidak menggantikan pemeriksaan server atas kepemilikan dan visibilitas repo. Pada bounty ini, screenshot yang belum dibuat berarti persiapan submit belum lengkap.

**Checklist sebelum menekan Submit:**

- [ ] Akun GitHub terhubung dan memiliki repo publik yang dibuat pada waktu yang diizinkan.
- [ ] Root berisi `README.md`, lisensi OSI, dan screenshot halaman GitHub sendiri sesuai aturan.
- [ ] Tidak ada `.github/README.md`; kode referral dan ketiga badge live benar.
- [ ] GitHub About sudah memakai website bounty dan topic `makefun`.
- [ ] Draf dan revisi tercatat dalam sesi agent; bundel berisi seluruh sesi serta konteks yang diwajibkan.
- [ ] Commit yang diperiksa sama dengan commit yang sudah dipush dan akan dikirim.
- [ ] Check sudah dijalankan, masalahnya diperbaiki, dan masih ada waktu serta kuota submit.

Kamu dapat memakai formulir **Enter** di halaman bounty: isi URL repo publik, pilih commit, dan unggah bundel. Jalur CLI untuk pemilik repo ini:

```sh
ENTRY_COMMIT=$(git -C ../makefun-bring-the-humans-02 rev-parse HEAD)
node cli/makefun.mjs submit \
  --competition bring-the-humans-02 \
  --repo-url https://github.com/0xyfann/makefun-bring-the-humans-02 \
  --commit "$ENTRY_COMMIT" \
  --title "Dari akun baru ke entri pertama" \
  --bundle transcripts.tar.gz \
  --keypair "$HOME/.makefun/keypairs/https_make.fun.json"
```

Wallet tersebut harus terhubung ke akun peserta. Untuk bounty dengan reward escrow, tanda tangan mengikat kompetisi, repo, commit, dan hash transkrip; wallet penandatangan adalah tujuan klaim sesuai aturan bounty ini. Pastikan commit itu sudah tersedia di GitHub sebelum submit.

## 6. Baca status dan perbaiki masalah

```sh
node cli/makefun.mjs status
```

Simpan receipt submit dan baca hasil check. Jika entri ditolak, status menjelaskan pemeriksaan yang gagal beserta perbaikannya. Perbaiki berkas, commit dan push perubahan, buat bundel yang sesuai, jalankan check lagi, lalu submit ulang sebelum tenggat.

Push baru saja tidak mengubah entri yang sudah diambil snapshot-nya. Untuk `bring-the-humans-02`, submit paling baru yang memiliki receipt sebelum deadline menjadi entri final, dengan batas 5 submit per hari UTC dan 10 total. Jangan menghabiskan kuota hanya untuk mencoba entri yang masih diketahui kurang lengkap.

Repo harus tetap publik, tetap repo yang sama dan dimiliki akun GitHub yang sama, serta README di default branch harus tetap membawa kode referral hingga re-check final. Hasil sementara belum merupakan keputusan akhir.

| Masalah yang kamu temui | Langkah perbaikan |
| --- | --- |
| GitHub menampilkan README yang berbeda | Pastikan nama file root tepat `README.md` dan tidak ada `.github/README.md`. |
| Badge tidak menuju repo sendiri | Periksa owner, nama repo, dan slug bounty pada URL gambar serta tautannya. |
| `guide_page` gagal karena gambar belum ada | Publikasikan repo, ambil screenshot halaman GitHub sendiri, commit dan push `screenshot.png`, lalu check ulang. |
| `bundle` berhenti karena konteks kurang | Baca detail yang diminta, lengkapi dari rekaman asli atau konfigurasi yang diketahui, lalu ulangi; jangan mengisi dengan perkiraan. |
| Perubahan terbaru belum tercermin di entri | Push commit baru dan submit ulang beserta bundel yang sesuai; simpan receipt baru. |

## 7. Klaim jika mendapat hadiah

Tunggu hasil final dan periksa status entri serta informasi payout. Posisi di leaderboard saja belum cukup untuk menyimpulkan ada hadiah. Bila reward tersedia, buka notifikasi atau profil make.fun dan ikuti proses klaim; hadiah perlu diklaim, bukan diasumsikan akan terkirim sendiri.

Untuk bounty ini yang menggunakan escrow, klaim dari escrow ke wallet yang menandatangani entri pemenang. Simpan keypair itu sampai proses selesai. Gunakan antarmuka klaim atau lihat sintaks CLI yang sesuai sebelum menjalankannya:

```sh
node cli/makefun.mjs claim --help
```

Pembayaran berupa **USDC pada Solana**. Klaim melalui pemeriksaan sanksi dan meminta informasi yang diwajibkan prosesnya; jawab pertanyaan status pajak sesuai keadaanmu. Ikuti batas waktu klaim yang ditampilkan bounty dan status klaim, bukan tenggat yang ditebak dari kompetisi lain. Bounty lama tanpa escrow mempunyai alur pembayaran berbeda; baca bagian **Payout** masing-masing.

## Bagaimana referral dihitung?

Di profil, tab **Referrals** menampilkan kode, tautan, nilai reward yang berlaku, dan statusnya. Tautan panduan ini adalah **https://make.fun/r/p1x954ca**, dengan kode **`p1x954ca`**.

Untuk bounty ini, referral mengikuti kode yang pertama terlihat oleh browser selama 60 hari; tautan lain yang dikunjungi belakangan tidak menggantikannya. Akun baru harus dibuat dalam jendela kompetisi dan lolos verifikasi. Akun sendiri, bot, serta signup yang tidak memenuhi pemeriksaan aktivitas dan jaringan tidak dihitung.

Reward referral program dan skor kompetisi bukan hal yang sama: batas reward signup program tidak membatasi skor signup yang sudah terverifikasi dalam kontes ini. Jangan membuat akun palsu untuk mengejar angka. Ajak orang yang memang ingin membaca aturan dan ikut membangun.

Jika panduan ini membantu, [mulai lewat referral p1x954ca](https://make.fun/r/p1x954ca), pilih satu tugas yang realistis, dan selesaikan entri pertamamu dengan rapi.

## Sumber resmi

Fakta dan contoh disusun dengan merujuk kit `bring-the-humans-02` serta dokumentasi resmi yang diperiksa pada **19 November 2026**. Angka reward, deadline, dan pemeriksaan bisa berubah; selalu baca halaman serta requirements bounty saat akan submit.

- [make.fun — papan bounty](https://make.fun)
- [Penjelasan alur platform](https://make.fun/how-it-works)
- [Panduan untuk coding agent](https://make.fun/skill.md)
- [Panduan membangun dengan AI agent](https://make.fun/guide/make-money-with-ai-agents)
- [Aturan dan halaman Bring the humans again](https://make.fun/bounty/bring-the-humans-02)
- [Requirements terkini bounty ini](https://make.fun/api/competitions/bring-the-humans-02/requirements)

Panduan komunitas oleh [0xyfann](https://github.com/0xyfann), dirilis dengan [lisensi MIT](LICENSE).
