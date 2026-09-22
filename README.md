# Pertemuan 04 - Seleksi Multi-Kondisi dan Validasi Input
## Identitas

| Keterangan        | Data                                  |
| ----------------- | ------------------------------------- |
| **Nama**          | Farid Syahputra                       |
| **NIM**           | 2225250222                            |
| **Program Studi** | S1 Pendidikan Matematika FKIP Untirta |
| **Mata Kuliah**   | Algoritma dan Pemrograman             |
| **Pertemuan**     | 04                                    |

## Deskripsi

Repository ini berisi tugas dan latihan pada **Pertemuan 04 — Validasi** mata kuliah Algoritma dan Pemrograman.

Materi yang dikerjakan berfokus pada penerapan validasi dalam program untuk memastikan data atau input yang diberikan sesuai dengan ketentuan yang telah ditentukan.

---

## Tujuan

Pada pertemuan ini saya mempelajari penggunaan seleksi multi-kondisi menggunakan `if`, `elif`, dan `else`, serta validasi input berdasarkan tipe dan rentang nilai.

Program yang dibuat digunakan untuk melakukan klasifikasi nilai, kategori bilangan, validasi rentang, validasi tipe data, klasifikasi segitiga berdasarkan sudut, serta validasi dan klasifikasi nilai akhir mahasiswa.

---

## Struktur Folder

```text
pertemuan-04-validasi-2225250222/
│
├── README.md
├── .gitignore
│
├── latihan/
│   ├── 01_predikat_nilai.py
│   ├── 02_kategori_bilangan.py
│   ├── 03_validasi_rentang.py
│   ├── 04_validasi_tipe.py
│   └── 05_klasifikasi_segitiga_sudut.py
│
└── praktik/
    └── validasi_klasifikasi_nilai.py
```

---

## Cara Menjalankan

Program dapat dijalankan melalui terminal menggunakan Python.

Contoh menjalankan latihan:

```bash
python latihan/01_predikat_nilai.py
```

```bash
python latihan/02_kategori_bilangan.py
```

```bash
python latihan/03_validasi_rentang.py
```

```bash
python latihan/04_validasi_tipe.py
```

```bash
python latihan/05_klasifikasi_segitiga_sudut.py
```

Untuk menjalankan Praktik 1:

```bash
python praktik/validasi_klasifikasi_nilai.py
```

---

## Tabel Keputusan Predikat Nilai

| Predikat | Rentang Nilai |
| -------- | ------------: |
| A        |         >= 85 |
| B        |         >= 70 |
| C        |         >= 60 |
| D        |         >= 50 |
| E        |          < 50 |

---

## Praktik 1

Praktik 1 menggunakan tiga input:

1. Nilai ujian
2. Nilai tugas
3. Persentase kehadiran

Nilai akhir dihitung menggunakan rumus:

```text
Nilai akhir = 0.6 × nilai ujian + 0.4 × nilai tugas
```

Nilai ujian, tugas, dan kehadiran harus berada pada rentang `0 sampai 100`.

Kehadiran minimal adalah `80%`. Jika kehadiran kurang dari 80%, mahasiswa dinyatakan:

```text
Tidak memenuhi syarat kehadiran
```

Jika memenuhi syarat kehadiran, nilai akhir diklasifikasikan menjadi predikat A sampai E.

Predikat A, B, dan C memiliki status:

```text
Lulus
```

Sedangkan predikat D dan E memiliki status:

```text
Belum lulus
```

Ketentuan tersebut mengikuti spesifikasi Praktik 1 pada bahan ajar.

---

## Hasil Pengujian

| No | Ujian | Tugas | Kehadiran | Hasil                                 |
| -: | ----: | ----: | --------: | ------------------------------------- |
|  1 |    90 |    80 |        95 | 86.00 — A — Lulus                     |
|  2 |    75 |    70 |        85 | 73.00 — B — Lulus                     |
|  3 |    60 |    60 |        80 | 60.00 — C — Lulus                     |
|  4 |    55 |    50 |        90 | 53.00 — D — Belum lulus               |
|  5 |    40 |    30 |       100 | 36.00 — E — Belum lulus               |
|  6 |    90 |    90 |        75 | Tidak memenuhi syarat kehadiran       |
|  7 |   105 |    80 |        90 | Ditolak — nilai ujian di luar rentang |
|  8 |    80 |    -5 |        90 | Ditolak — nilai tugas di luar rentang |
|  9 |    80 |    80 |       abc | Ditolak — input harus berupa angka    |

Test case tersebut merupakan test case yang ditentukan dalam bahan ajar Praktik 1.

---

## Validasi Input

Program menggunakan `try-except ValueError` untuk menangani input yang bukan berupa angka.

Selain validasi tipe data, program juga melakukan validasi rentang untuk memastikan nilai ujian, tugas, dan kehadiran berada pada rentang `0 sampai 100`.

Validasi dilakukan sebelum proses perhitungan dan klasifikasi.

---

## Refleksi

Dari praktik ini saya memahami bahwa seleksi `if-elif-else` dapat digunakan untuk menentukan satu kondisi yang sesuai dari beberapa kondisi yang tersedia.

Saya juga memahami pentingnya validasi input sebelum data diproses. Dengan validasi tipe dan rentang, program dapat menolak input yang tidak sesuai sehingga hasil program lebih terkontrol.

Pada Praktik 1, pemeriksaan kehadiran dilakukan sebelum menentukan predikat. Hal ini membuat kondisi kehadiran menjadi salah satu syarat utama sebelum status kelulusan ditentukan.

---

## Kesimpulan

Pada Pertemuan 04 saya telah menerapkan seleksi multi-kondisi dan validasi input menggunakan Python. Program yang dibuat mencakup klasifikasi nilai, kategori bilangan, validasi rentang, validasi tipe data, klasifikasi segitiga berdasarkan sudut, serta validasi dan klasifikasi nilai akhir mahasiswa.
