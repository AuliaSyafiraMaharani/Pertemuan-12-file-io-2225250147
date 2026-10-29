# Pertemuan 12: File I/O dan Error Handling

Nama: Aulia Syafira Maharani  
NIM: 2225250147
Kelas: 3A  

## Tujuan
Membaca, memvalidasi, mengolah, dan menulis data file dengan Python[cite: 13].

## Format File Input
NIM, nilai[cite: 13]

## Cara Menjalankan
```bash
python3 tugas/rekap_nilai_file.py
```[cite: 13]

## Error yang Ditangani
- `FileNotFoundError`[cite: 13]
- `ValueError`[cite: 13]

## Test Case
| Kondisi | Hasil yang Diharapkan | Hasil Aktual | Status |
| :--- | :--- | :--- | :--- |
| Normal (Semua baris valid) | Semua record diproses dan rekap benar[cite: 12] | Sesuai | Lulus |
| File hilang (`nilai.txt` tidak ada) | Pesan file tidak ditemukan; program tidak crash[cite: 12] | Sesuai | Lulus |
| Nilai invalid (`A004, abc`) | Baris invalid dilewati/dilaporkan; record lain tetap diproses[cite: 12] | Sesuai | Lulus |
| Baris kosong | Baris kosong dilewati[cite: 12] | Sesuai | Lulus |
| Batas lulus (Nilai 60) | Dihitung sebagai lulus[cite: 12] | Sesuai | Lulus |

## Refleksi
Error `ValueError` yang terjadi ketika data nilai berupa teks (misalnya `abc`) berhasil diatasi dengan menangani exception secara spesifik per baris menggunakan struktur `try-except`, sehingga program tidak berhenti secara kasar dan data baris valid lainnya tetap dapat diproses dengan baik.