# Pertemuan-pemrograman 12
class DaftarNilaiMahasiswa:
    def _init_(self):
        self.data_mahasiswa = []

    def tambah(self, nama, nilai):
        self.data_mahasiswa.append({'nama': nama, 'nilai': nilai})
        print(f"Data {nama} berhasil ditambahkan!")

    def tampilkan(self):
        print("\nDaftar Nilai Mahasiswa:")
        if not self.data_mahasiswa:
            print("Belum ada data mahasiswa.")
        else:
            for i, data in enumerate(self.data_mahasiswa, start=1):
                print(f"{i}. Nama: {data['nama']}, Nilai: {data['nilai']}")

    def hapus(self, nama):
        for data in self.data_mahasiswa:
            if data['nama'].lower() == nama.lower():
                self.data_mahasiswa.remove(data)
                print(f"Data {nama} berhasil dihapus!")
                return
        print(f"Data {nama} tidak ditemukan!")

    def ubah(self, nama, nilai_baru):
        for data in self.data_mahasiswa:
            if data['nama'].lower() == nama.lower():
                data['nilai'] = nilai_baru
                print(f"Data {nama} berhasil diubah menjadi Nilai: {nilai_baru}")
                return
        print(f"Data {nama} tidak ditemukan!")


if _name_ == "_main_":
    daftar_nilai = DaftarNilaiMahasiswa()

    while True:
        print("\nMenu:")
        print("1. Tambah Data")
        print("2. Tampilkan Data")
        print("3. Hapus Data")
        print("4. Ubah Data")
        print("5. Keluar")
        
        pilihan = input("Pilih menu (1-5): ")
        
        if pilihan == '1':
            nama = input("Masukkan Nama Mahasiswa: ")
            nilai = float(input("Masukkan Nilai Mahasiswa: "))
            daftar_nilai.tambah(nama, nilai)
        
        elif pilihan == '2':
            daftar_nilai.tampilkan()
        
        elif pilihan == '3':
            nama = input("Masukkan Nama Mahasiswa yang akan dihapus: ")
            daftar_nilai.hapus(nama)
        
        elif pilihan == '4':
            nama = input("Masukkan Nama Mahasiswa yang akan diubah: ")
            nilai_baru = float(input("Masukkan Nilai Baru: "))
            daftar_nilai.ubah(nama, nilai_baru)
        
        elif pilihan == '5':
            print("Program selesai. Terima kasih!")
            break
        
        else:
            print("Pilihan tidak valid! Silakan pilih menu 1-5.")



Program Pengelolaan Nilai Mahasiswa
Deskripsi
Program ini dibuat untuk mengelola daftar nilai mahasiswa dengan mengaplikasikan pengguanaan class. Program ini mempunyai beberapa fungsi:

tambah(): Menambahkan data mahasiswa.
tampilkan(): Menampilkan seluruh data mahasiswa.
hapus(nama): Menghapus data mahasiswa berdasarkan nama.
ubah(nama): Mengubah data mahasiswa berdasarkan nama.
Cara Penggunaan
Jalankan program. lalu pilih menu yang tersedia:

Tambah Data: Masukkan data baru Nama dan Nilai.
Tampilkan Data: Lihat semua data mahasiswa.
Hapus Data: Hapus data berdasarkan nama mahasiswa.
Ubah Data: Edit data mahasiswa yang sudah ada.
Keluar: Mengakhiri program.

Screenshoot

![Screenshot 2025-01-02 211224](https://github.com/user-attachments/assets/e8e37791-bd22-4da7-a64e-bc7fa06a5b8b)
![Screenshot 2025-01-02 211246](https://github.com/user-attachments/assets/2cd22a9e-7af3-439d-afd6-408bee8f0ed8)
![Screenshot 2025-01-02 211318](https://github.com/user-attachments/assets/de6391b9-6c81-487b-b310-8ae28f090e06)
![Screenshot 2025-01-02 211333](https://github.com/user-attachments/assets/99155e63-93a8-4cbd-859f-851bf34df231)
![Screenshot 2025-01-02 211347](https://github.com/user-attachments/assets/9d2e33d5-87ce-4322-9b9e-7332140ff76d)
![Screenshot 2025-01-02 211401](https://github.com/user-attachments/assets/d9413218-8e17-4f14-9666-12fd50bd97e4)
![Screenshot 2025-01-02 211413](https://github.com/user-attachments/assets/e52138bc-2f8a-43cd-b7a1-ca2a9bad7032)
![Screenshot 2025-01-02 211432](https://github.com/user-attachments/assets/71c235c5-048c-49e2-9e0d-eaa025be84d0)








Flowchart
![Screenshot 2025-01-02 205640](https://github.com/user-attachments/assets/7694085a-73fa-4c93-b190-041c96638296)
