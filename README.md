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
flowchart:

![Screenshot 2024-11-15 172233](https://github.com/user-attachments/assets/626f967c-f5eb-49f8-a775-41da32d82c6b)

#latihan 

    Buat sebuah list sebanyak 5 elemen dengan nilai bebas
    • akses list:
    • tampilkan elemen ke 3
    • ambil nilai elemen ke 2 sampai elemen ke 4
    • ambil elemen terakhir
    • ubah elemen list:
    • ubah elemen ke 4 dengan nilai lainnya
    • ubah elemen ke 4 sampai dengan elemen terakhir
    • tambah elemen list:
    • ambil 2 bagian dari list pertama (A) dan jadikan list ke 2 (B)
    • tambah list B dengan nilai string
    • tambah list B dengan 3 nilai
    • gabungkan list B dengan list A

kode program : 

    # Membuat list dengan 5 elemen
    list_A = [5, 10, 15, 20, 25]  # Nilai bebas
    
    # Akses list
    # Tampilkan elemen ke 3
    print("Elemen ke-3:", list_A[2])  # Indeks 2 adalah elemen ke-3
    
    # Ambil nilai elemen ke 2 sampai elemen ke 4
    sub_list = list_A[1:4]  # Indeks 1 sampai 3 (elemen ke-2 sampai ke-4)
    print("Nilai elemen ke-2 sampai ke-4:", sub_list)
    
    # Ambil elemen terakhir
    last_element = list_A[-1]  # Elemen terakhir
    print("Elemen terakhir:", last_element)
    
    # Ubah elemen list
    # Ubah elemen ke 4 dengan nilai lainnya
    list_A[3] = 100  # Mengubah elemen ke-4 (indeks 3) menjadi 100
    print("List setelah mengubah elemen ke-4:", list_A)
    
    # Ubah elemen ke 4 sampai dengan elemen terakhir
    list_A[3:] = [200, 300]  # Mengubah elemen ke-4 sampai akhir
    print("List setelah mengubah elemen ke-4 sampai akhir:", list_A)
    
    # Tambah elemen list
    # Ambil 2 bagian dari list pertama (A) dan jadikan list ke 2 (B)
    list_B = list_A[0:2]  # Mengambil elemen ke-1 dan ke-2
    print("List B (bagian dari list A):", list_B)
    
    # Tambah list B dengan nilai string
    list_B.append("string")  # Menambahkan string ke list B
    print("List B setelah menambahkan string:", list_B)
    
    # Tambah list B dengan 3 nilai
    list_B.extend([400, 500, 600])  # Menambahkan 3 nilai ke list B
    print("List B setelah menambahkan 3 nilai:", list_B)
    
    # Gabungkan list B dengan list A
    combined_list = list_A + list_B  # Menggabungkan list A dan list B
    print("List gabungan A dan B:", combined_list)

output : 
![Screenshot 2024-11-15 174315](https://github.com/user-attachments/assets/a914c97c-d99e-416d-b01a-23be3bec7b18)

    penjelasan program : 
    1. membuat list
       -Tujuan: Membuat sebuah list bernama list_A yang berisi 5 elemen dengan nilai yang ditentukan secara bebas
       -Cara Kerja: List ini diinisialisasi dengan nilai-nilai integer (5, 10, 15, 20, 25).
    2. akses list
        a. tampilkan elemen ke-3
            - Tujuan: Menampilkan elemen ketiga dari list_A.
            - Cara Kerja: Menggunakan indeks 2 (karena pengindeksan di Python dimulai dari 0) untuk mengambil elemen ke-3, yang adalah 30.
        b.  Ambil Nilai Elemen ke-2 sampai Elemen ke-4
           - Tujuan: Mengambil dan menampilkan elemen dari indeks 1 sampai 3, yang mencakup elemen ke-2, ke-3, dan ke-4.
           - Cara Kerja: Menggunakan slicing list_A[1:4] untuk mendapatkan sublist yang berisi [20, 30, 40].
         c. ambil elemen terakhir 
           - Tujuan: Menampilkan elemen terakhir dari list_A.
           - Cara Kerja: Menggunakan indeks -1 untuk mengambil elemen terakhir, yang adalah 50
           3. ubah elemen list 
        a. ubah elemen ke-4 dengan nilai lain 
           - tujuan : mengubah nilai elemen ke-4 menjadi 100
           - cara kerja : mengakses elemen dengan indeks 3 dan menetapkannya ke nilai baru.
       b.  Ubah Elemen ke-4 sampai dengan Elemen Terakhir
          - Tujuan: Mengambil dan menampilkan elemen dari indeks 1 sampai 3, yang mencakup elemen ke-2, ke-3, dan ke-4.
          - Cara Kerja: Menggunakan slicing list_A[1:4] untuk mendapatkan sublist yang berisi [20, 30, 40].
    4. tambah elemen list 
       a.  Ambil 2 Bagian dari List Pertama (A) dan Jadikan List ke-2 (B)
        -Tujuan: Membuat list baru list_B yang berisi dua elemen pertama dari list_A.
        - Cara Kerja: Menggunakan slicing untuk mengambil elemen dari indeks 0 sampai 1, menghasilkan [10, 20].
      b. tambah list B dengan nilai string 
        -Tujuan: Menambahkan nilai string ke dalam list_B.
        - Cara Kerja: Menggunakan metode append untuk menambahkan "string" ke akhir list.
      c. tambah list B dengan 3 nilai 
        - Tujuan: Menambahkan tiga nilai baru ke list_B.
         - Cara Kerja: Menggunakan metode extend untuk menambahkan elemen [400, 500, 600] ke dalam list_B.
    5. gabungkan list B dengan list A
     




