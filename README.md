# praktikum5
    Buat program sederhana yang akan menampilkan daftar nilai mahasiswa, dengan ketentuan
    • Program dibuat dengan menggunakan Dictionary*
    • Tampilkan menu pilihan: (Tambah Data, Ubah Data, Hapus Data, Tampilkan Data, Cari Data)
    • Nilai Akhir diambil dari perhitungan 3 komponen nilai (tugas: 30%, uts: 35%, uas: 35%)
    • Buat flowchart dan penjelasan programnya pada README.md.
    • Commit dan push repository ke github.
# flowchart 
   ![Screenshot 2024-11-21 121454](https://github.com/user-attachments/assets/bd7eb0d9-a5a5-4d5c-954d-0de7b1d07cf7)
# kode program
![Screenshot 2024-11-20 231721](https://github.com/user-attachments/assets/389ebfa3-305e-4957-815c-42438306dc14)
![Screenshot 2024-11-20 231734](https://github.com/user-attachments/assets/68ceed99-0f42-4045-afb0-3448d640a48f)
![Screenshot 2024-11-20 231834](https://github.com/user-attachments/assets/b04a3334-988b-40b2-a107-4286955ad746)

# penjelasan program
1. Dictionary:
  - Disini Data mahasiswa disimpan dalam dictionary yang menggunakan NIM sebagai key dan data mahasiswa lainnya (nama, nilai tugas, UTS, UAS, nilai akhir) sebagai value 
    yang berupa dictionary.
2. Fungsi tambah data:
  - Meminta input NIM, nama, nilai tugas, UTS, dan UAS. Lalu, menghitung nilai akhir dan menyimpan data tersebut dalam dictionary data mahasiswa.
3. Fungsi ubah data:
 - Mengubah data mahasiswa yang sudah ada berdasarkan NIM. Jika NIM ditemukan, program akan meminta input nilai baru untuk tugas, UTS, dan UAS, serta menghitung ulang nilai 
   akhir.
4. Fungsi hapus data:
 - Menghapus data mahasiswa berdasarkan NIM yang dimasukkan. Jika NIM ditemukan, data akan dihapus dari dictionary.
5. Fungsi tampilkan data:
 - Menampilkan seluruh data mahasiswa yang ada dalam format tabel yang rapi, dengan informasi NIM, nama, nilai tugas, UTS, UAS, dan nilai akhir.
6. Fungsi cari data:
 - Mencari data mahasiswa berdasarkan NIM. Jika NIM ditemukan, data lengkap mahasiswa akan ditampilkan.
7. Menu Utama:
 - Program menampilkan menu pilihan (lihat, tambah, ubah, hapus, cari, keluar) dan mengeksekusi fungsi yang sesuai berdasarkan input pengguna.
# output 
![Screenshot 2024-11-20 230152](https://github.com/user-attachments/assets/6e4a9f9d-0c05-4dd8-880d-3e9e551ab41c)
![Screenshot 2024-11-20 230208](https://github.com/user-attachments/assets/15703261-2fef-4250-ace0-b13379cca682)
![Screenshot 2024-11-20 230218](https://github.com/user-attachments/assets/5254c1ab-eb4e-4998-af46-e1554e4c389c)

# latihan 1 
kode program
input :

    #1. Buat Dictionary daftar kontak
    daftar_kontak = {
        "ajeng": "08987654321",
        "iqbal": "08234567890",
        "udin": "08345678901"
    }
    
    # 2. Tampilkan kontaknya Ari
    print("Kontak ajeng:", daftar_kontak.get("Ajeng"))
    
    # 3. Tambah kontak baru dengan nama Riko, nomor 087654544
    daftar_kontak["rafif"] = "08898917665"
    print("Kontak Rafif telah ditambahkan.")
    
    # 4. Ubah kontak Dina dengan nomor baru 088999776
    daftar_kontak["fiyaa"] = "088999776"
    print("Kontak fiya telah diubah.")
    
    # 5. Tampilkan semua Nama
    print("Semua Nama:", list(daftar_kontak.keys()))
    
    # 6. Tampilkan semua Nomor
    print("Semua Nomor:", list(daftar_kontak.values()))
    
    # 7. Tampilkan daftar Nama dan nomornya
    print("Daftar Nama dan Nomornya:")
    for nama, nomor in daftar_kontak.items():
        print(f"{nama}: {nomor}")
    
    # 8. Hapus kontak Dina
    if "Dina" in daftar_kontak:
        del daftar_kontak["Dina"]
        print("Kontak Dina telah dihapus.")
    else:
        print("Kontak Dina tidak ditemukan.")
# penjelasan program 
    1. Membuat Dictionary Daftar Kontak:
        - Di sini, kita membuat sebuah dictionary bernama daftar kontak yang berisi nama-nama kontak sebagai kunci (key) dan nomor telepon mereka sebagai nilai (value).
    2. menampilkan kontak ajeng : 
        - Pada langkah ini, kita mencoba untuk menampilkan nomor telepon dari kontak bernama "Ajeng". Namun, perlu dicatat bahwa nama "Ajeng" ditulis dengan huruf besar, 
          sedangkan dalam dictionary kita menggunakan huruf kecil. Oleh karena itu, output akan None karena "Ajeng" tidak ditemukan.
    3. menambah kontak baru : 
        - Di sini, kita menambahkan kontak baru dengan nama "rafif" dan nomor telepon "08898917665" ke dalam dictionary. Pesan konfirmasi ditampilkan untuk menunjukkan 
          bahwa kontak tersebut telah berhasil ditambahkan.
    4. mengubah kontak fiyaa:
        - Pada langkah ini, kita menambahkan atau memperbarui kontak "fiyaa" dengan nomor telepon "088999776". Jika kontak tersebut sudah ada, nomor lama akan diganti 
          dengan yang baru.
    5. menampilkan semua nama : 
        - Kita menggunakan daftar_kontak.keys() untuk mendapatkan semua nama kontak yang ada dalam dictionary dan mengubahnya menjadi list. Hasilnya ditampilkan ke layar. 
    6. menampilkan semua nomor : 
        - Di sini, kita menggunakan daftar_kontak.values() untuk mendapatkan semua nomor telepon yang ada dalam dictionary dan mengubahnya menjadi list. Hasilnya juga 
          ditampilkan ke layar.
    7. menampilkan daftar nama dan nomornya:
        - Kita menggunakan daftar_kontak.items() untuk mendapatkan pasangan kunci-nilai (nama-nomor) dalam dictionary. Dengan menggunakan loop for, kita mencetak setiap 
          nama beserta nomor teleponnya.
    8. menghapus kontak dina :
       - Pada langkah ini, kita memeriksa apakah kontak dengan nama "Dina" ada dalam dictionary. Jika ada, kita menghapusnya menggunakan del. Jika tidak, pesan yang 
         menyatakan bahwa kontak tidak ditemukan akan ditampilkan. Namun, dalam kode ini, "Dina" tidak ada dalam dictionary, jadi output yang akan muncul adalah "Kontak 
          Dina tidak ditemukan."

output : 
![Screenshot 2024-11-21 104305](https://github.com/user-attachments/assets/04ea8887-28b5-4802-ab38-f11ef22eb880)



   
