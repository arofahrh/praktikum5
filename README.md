# praktikum5
    Buat program sederhana yang akan menampilkan daftar nilai mahasiswa, dengan ketentuan
    • Program dibuat dengan menggunakan Dictionary*
    • Tampilkan menu pilihan: (Tambah Data, Ubah Data, Hapus Data, Tampilkan Data, Cari Data)
    • Nilai Akhir diambil dari perhitungan 3 komponen nilai (tugas: 30%, uts: 35%, uas: 35%)
    • Buat flowchart dan penjelasan programnya pada README.md.
    • Commit dan push repository ke github.
# kode program
    # Dictionary untuk menyimpan data mahasiswa
    data_mahasiswa = {}
    
    # Fungsi untuk menambahkan data mahasiswa
    def tambah_data():
        print("\nTambah Data")
        nim = input("NIM  : ")
        nama = input("Nama : ")
        tugas = float(input("Nilai Tugas: "))
        uts = float(input("Nilai UTS: "))
        uas = float(input("Nilai UAS: "))
        nilai_akhir = tugas * 0.3 + uts * 0.35 + uas * 0.35
        data_mahasiswa[nim] = {"nama": nama, "tugas": tugas, "uts": uts, "uas": uas, "akhir": nilai_akhir}
        print("Data berhasil ditambahkan!")

    # Fungsi untuk mengubah data mahasiswa
    def ubah_data():
        print("\nUbah Data")
        nim = input("Masukkan NIM mahasiswa: ")
        if nim in data_mahasiswa:
            print(f"Nama: {data_mahasiswa[nim]['nama']}")
            data_mahasiswa[nim]['tugas'] = float(input("Nilai Tugas Baru: "))
            data_mahasiswa[nim]['uts'] = float(input("Nilai UTS Baru: "))
            data_mahasiswa[nim]['uas'] = float(input("Nilai UAS Baru: "))
            data_mahasiswa[nim]['akhir'] = data_mahasiswa[nim]['tugas'] * 0.3 + data_mahasiswa[nim]['uts'] * 0.35 + data_mahasiswa[nim]['uas'] * 0.35
            print("Data berhasil diubah!")
        else:
            print("NIM tidak ditemukan!")

    # Fungsi untuk menghapus data mahasiswa
    def hapus_data():
        print("\nHapus Data")
        nim = input("Masukkan NIM mahasiswa: ")
        if nim in data_mahasiswa:
            del data_mahasiswa[nim]
            print("Data berhasil dihapus!")
        else:
            print("NIM tidak ditemukan!")

    # Fungsi untuk menampilkan data mahasiswa
    def tampilkan_data():
        print("\nDaftar Nilai")
        print("=========================================")
        print("| NO |  NIM  |  Nama  | Tugas | UTS | UAS | Akhir |")
        print("=========================================")
        for i, (nim, data) in enumerate(data_mahasiswa.items(), start=1):
            print(f"| {i:<2} | {nim:<6} | {data['nama']:<6} | {data['tugas']:<5} | {data['uts']:<3} | {data['uas']:<3} | {data['akhir']:<5.2f} |")
        print("=========================================")

    # Fungsi untuk mencari data mahasiswa
    def cari_data():
        print("\nCari Data")
        nim = input("Masukkan NIM mahasiswa: ")
        if nim in data_mahasiswa:
            print("Data ditemukan!")
            print(f"NIM   : {nim}")
            print(f"Nama  : {data_mahasiswa[nim]['nama']}")
            print(f"Tugas : {data_mahasiswa[nim]['tugas']}")
            print(f"UTS   : {data_mahasiswa[nim]['uts']}")
            print(f"UAS   : {data_mahasiswa[nim]['uas']}")
            print(f"Akhir : {data_mahasiswa[nim]['akhir']:.2f}")
        else:
            print("NIM tidak ditemukan!")

    # Menu utama
    while True:
        print("\nProgram Input Nilai")
        print("===================")
        pilihan = input("[(L)ihat, (T)ambah, (U)bah, (H)apus, (C)ari, (K)eluar]: ").lower()
        if pilihan == "l":
            tampilkan_data()
        elif pilihan == "t":
            tambah_data()
        elif pilihan == "u":
            ubah_data()
        elif pilihan == "h":
            hapus_data()
    elif pilihan == "c":
        cari_data()
    elif pilihan == "k":
        print("Program selesai.")
        break
    else:
        print("Pilihan tidak valid!")
