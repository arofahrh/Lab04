# praktikum 4 
    1. Buatlah program sederhana untuk menambahkan data kedalam sebuah list dengan rincian sebagai berikut :
    2. Program meminta memasukkan data sebanyak-banyakanya (gunakan perulangan)
    3. Tampilkan pertanyaan untuk menambahkan data (y/t?), apabila jawaban t (tidak), maka program akan menampilkan daftar datanya
    4. Nilai akhir diambil dari perhitungan 3 komponen nilai (tugas: 30%, uts:35%, uas:35%)
    5. Buat flowchart
  code program : 

     # Inisialisasi list untuk menyimpan data
    data_mahasiswa = []
    
    while True:
        # Input data mahasiswa
        nama = input("Nama mahasiswa: ")
        tugas = float(input("Nilai tugas: "))
        uts = float(input("Nilai UTS: "))
        uas = float(input("Nilai UAS: "))
        # Hitung nilai akhir
        nilai_akhir = (tugas * 0.3) + (uts * 0.35) + (uas * 0.35)
        # Simpan data ke dalam list
        data_mahasiswa.append({
            'nama': nama,
            'tugas': tugas,
            'uts': uts,
            'uas': uas,
            'nilai_akhir': nilai_akhir
        })
        # Tanyakan apakah ingin menambah data
        tambah_data = input("Apakah ada data yang ingin ditambahkan? (y/t): ")
        if tambah_data.lower() == 't':
            break
    
    # Tampilkan daftar data
    print("\nDaftar Data Mahasiswa:")
    print("================================================")
    print("| No | Nama              | Tugas | UTS | UAS | Akhir |")
    print("================================================")
    for i, mahasiswa in enumerate(data_mahasiswa):
        print(f"| {i+1:<2} | {mahasiswa['nama']:<16} | {mahasiswa['tugas']:<5} | {mahasiswa['uts']:<3} | {mahasiswa['uas']:<3} | {mahasiswa['nilai_akhir']:.2f} |")
    print("================================================")

  input dan output : 
  ![Screenshot 2024-11-14 192455](https://github.com/user-attachments/assets/6058ba32-6617-4d52-943a-1fc0c69aaacd)

      penjelasan program : 
    1. Inisialisasi List
       - Program dimulai dengan mendeklarasikan sebuah list kosong bernama data_mahasiswa. List ini akan digunakan untuk menyimpan data mahasiswa yang akan dimasukkan oleh 
         pengguna.
    2. Loop untuk input data
       - Program menggunakan loop while True untuk terus meminta input data dari pengguna. Loop ini akan berjalan terus hingga pengguna memilih untuk berhenti.
       - Setelah pengguna memasukkan data mahasiswa, program akan menanyakan apakah mereka ingin menambah data lagi. Jika pengguna menjawab 't' (tidak), loop akan berhenti.
    3. input data mahasiswa
       - Di dalam loop, program meminta pengguna untuk memasukkan nama mahasiswa dan nilai untuk tugas, UTS, dan UAS. Nilai-nilai ini diambil sebagai input bertipe float agar 
         dapat melakukan perhitungan yang tepat.
    4. menghitung nilai akhir
       -Setelah mendapatkan nilai tugas, UTS, dan UAS, program menghitung nilai akhir dengan menggunakan rumus yang telah ditentukan:
         30% dari nilai tugas
         35% dari nilai UTS
          35% dari nilai UAS
       -Hasil perhitungan disimpan dalam variabel nilai_akhir.
    5. menyimpan data
       -Program menyimpan data mahasiswa (nama dan nilai) dalam bentuk dictionary dan menambahkannya ke dalam list data_mahasiswa. Setiap dictionary berisi informasi tentang 
        satu mahasiswa.
    6. menampilkan daftar data
       - Setelah loop selesai, program mencetak daftar mahasiswa beserta nilainya dalam format tabel.
       - Header tabel ditampilkan dengan garis pemisah untuk meningkatkan keterbacaan.
       - Menggunakan enumerate, program memberikan nomor urut untuk setiap mahasiswa dan mencetak data mereka dalam format yang teratur.


