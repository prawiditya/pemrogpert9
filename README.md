
# PRAWIDITYA SAHRUL AKBAR
# NIM 312410146
# Program Menghitung Data Nilai Akhir Mahasiswa
Program ini merupakan berbasis list yang digunakan untuk menyimpan dan menghitung nilai akhir mahasiswa. 
Nilai akhir dihitung berdasarkan bobot tertentu dari nilai tugas, UTS, dan UAS.
# Deskripsi Program
Program ini dibuat menggunakan bahasa python dengan fitur:
- List dan Dictionary untuk penyimpanan data.
- Fungsi Kustom (def) untuk perhitungan nilai akhir.
- input() dan int() untuk input dan konversi data.
- while dan if untuk kontrol alur.
- append() dan break untuk menambah data ke list dan menghentikan perulangan.
- print() dan F-string untuk mencetak hasil dalam bentuk tabel yang terformat.
## Flowchart Programan
![WhatsApp Image 2024-11-17 at 11 19 34_ccadbee7](https://github.com/user-attachments/assets/095df077-32b2-41e2-a08c-82fc4fcc8d85)
# Kode Program

```python
def hitung_nilai_akhir(nilai_tugas_values, nilai_uts_values, nilai_uas_values ):
    nilai_akhir = (nilai_tugas_values * 0.30) + (nilai_uts_values *0.35) + (nilai_uas_values *0.35)
    return round(nilai_akhir, 2)  # Membulatkan hasil ke dua tempat desimal

# Hasil untuk menyimpan data
nama = []
nim = []
nilai_tugas = []
nilai_uts = []
nilai_uas = []
nilai_akhir_values = []

while True:
    # input data mahasiswa 
    nama_values = input ("Nama: ") 
    nim_values = input ("NIM: ")
    try:
        nilai_tugas_values = float(input("Nilai Tugas: "))
        nilai_uts_values = float(input("Nilai UTS: "))
        nilai_uas_values = float(input("Nilai UAS: "))
    except ValueError:
        print("Masukkan nilai dengan format yang benar (angka). Coba lagi.")
        continue

    #Hitung nilai akhir
    nilai_akhir = hitung_nilai_akhir(nilai_tugas_values, nilai_uts_values, nilai_uas_values)

    # Simpan data 
    nama.append(nama_values)
    nim.append(nim_values)
    nilai_tugas.append(nilai_tugas_values)
    nilai_uts.append(nilai_uts_values) 
    nilai_uas.append(nilai_uas_values)
    nilai_akhir_values.append(nilai_akhir)

    # Tanya apakah ingin menambah data lagi 
    tambah_data = input("Apakah anda ingin menambah data lagi? (y/t): ")
    if tambah_data == 't':
        break

# Output daftar mahasiswa
print("\nDaftar Mahasiswa: ")
print(f"{'Nama':<20} | {'NIM':<10} | {'Tugas':<10} | {'UTS':<10} | {'UAS':<10} | {'Nilai Akhir':<10}")
print("=" *80)

# Menampilkan semua data yang sudah dimasukkan 
for i in range(len(nama)):
    print(f"{nama[i]:<20} {nim[i]:<13} {nilai_tugas[i]:<11} {nilai_uts[i]:<13} {nilai_uas[i]:<13} {nilai_akhir_values[i]:<10}")
```
# Output Program

```
# Cara Kerja Program
1. Program pertama kali menginisialisasi list kosong bernama data_mahasiswa untuk menyimpan data setiap mahasiswa.
2. Fungsi hitung_nilai_akhir digunakan untuk menghitung nilai akhir berdasarkan formula:
   \[
   \text{nilai akhir} = (\text{nilai tugas} \times 0.3) + (\text{nilai UTS} \times 0.35) + (\text{nilai UAS} \times 0.35)
   \]
3. Program meminta pengguna untuk memasukkan data nama, NIM, nilai tugas, UTS, dan UAS.
4. Setelah nilai akhir dihitung menggunakan fungsi hitung_nilai_akhir, semua data tersebut disimpan dalam dictionary dan ditambahkan ke dalam list data_mahasiswa.
5. Pengguna dapat memilih untuk menambahkan data mahasiswa lain atau mengakhiri proses input.
6. Setelah input selesai, program akan mencetak data mahasiswa dalam bentuk tabel dengan kolom nomor, nama, NIM, nilai tugas, UTS, UAS, dan nilai akhir.# Program Menghitung Data Nilai Akhir Mahasiswa
Program ini merupakan berbasis list yang digunakan untuk menyimpan dan menghitung nilai akhir mahasiswa. 
Nilai akhir dihitung berdasarkan bobot tertentu dari nilai tugas, UTS, dan UAS.
# Deskripsi Program
Program ini dibuat menggunakan bahasa python dengan fitur:
- List dan Dictionary untuk penyimpanan data.
- Fungsi Kustom (def) untuk perhitungan nilai akhir.
- input() dan int() untuk input dan konversi data.
- while dan if untuk kontrol alur.
- append() dan break untuk menambah data ke list dan menghentikan perulangan.
- print() dan F-string untuk mencetak hasil dalam bentuk tabel yang terformat.
## Flowchart Programan

# Kode Program
```python
# Inisialisasi list untuk menyimpan data
data_mahasiswa = []

# Fungsi untuk menghitung nilai akhir
def hitung_nilai_akhir(tugas, uts, uas):
    return round((tugas * 0.3) + (uts * 0.35) + (uas * 0.35), 2)

## Input data mahasiswa
while True:
    nama = input("Nama: ")
    nim = input("NIM: ")
    tugas = int(input("Nilai Tugas: "))
    uts = int(input("Nilai UTS: "))
    uas = int(input("Nilai UAS: "))
    nilai_akhir = hitung_nilai_akhir(tugas, uts, uas)

    # Simpan data ke dalam dictionary
    data_mahasiswa.append({
        "Nama": nama,
        "NIM": nim,
        "Tugas": tugas,
        "UTS": uts,
        "UAS": uas,
        "Akhir": nilai_akhir
    })

    # Tanyakan apakah ingin menambah data lagi
    tambah = input("Tambah data (y/t)? ")
    if tambah.lower() != 'y':
        break

# Tampilkan data dalam bentuk tabel
print("\n| No | Nama     | NIM   | Tugas | UTS | UAS | Akhir |")
print("-" * 50)
for i, mhs in enumerate(data_mahasiswa, start=1):
    print(f"| {i:<2} | {mhs['Nama']:<8} | {mhs['NIM']:<5} | {mhs['Tugas']:<5} | {mhs['UTS']:<3} | {mhs['UAS']:<3} | {mhs['Akhir']:<5} |")
```
# Output Program
![WhatsApp Image 2024-11-17 at 11 27 58_785740a6](https://github.com/user-attachments/assets/7d99a036-2c28-4b0e-a5d1-fbcb2d0a0ab2)
## Cara Kerja Program
1. Program pertama kali menginisialisasi list kosong bernama data_mahasiswa untuk menyimpan data setiap mahasiswa.
2. Fungsi hitung_nilai_akhir digunakan untuk menghitung nilai akhir berdasarkan formula: [ \text{nilai akhir} = (\text{nilai tugas} \times 0.3) + (\text{nilai UTS} \times 0.35) + (\text{nilai UAS} \times 0.35) ]
3. Program meminta pengguna untuk memasukkan data nama, NIM, nilai tugas, UTS, dan UAS.
4. Setelah nilai akhir dihitung menggunakan fungsi hitung_nilai_akhir, semua data tersebut disimpan dalam dictionary dan ditambahkan ke dalam list data_mahasiswa.
5. Pengguna dapat memilih untuk menambahkan data mahasiswa lain atau mengakhiri proses input.
6. Setelah input selesai, program akan mencetak data mahasiswa dalam bentuk tabel dengan kolom nomor, nama, NIM, nilai tugas, UTS, UAS, dan nilai akhir
