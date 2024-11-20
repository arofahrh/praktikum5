# praktikum5
    Buat program sederhana yang akan menampilkan daftar nilai mahasiswa, dengan ketentuan
    • Program dibuat dengan menggunakan Dictionary*
    • Tampilkan menu pilihan: (Tambah Data, Ubah Data, Hapus Data, Tampilkan Data, Cari Data)
    • Nilai Akhir diambil dari perhitungan 3 komponen nilai (tugas: 30%, uts: 35%, uas: 35%)
    • Buat flowchart dan penjelasan programnya pada README.md.
    • Commit dan push repository ke github.
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


   
