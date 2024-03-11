import 'dart:async';

// Kelas untuk menggambarkan dan mendeskripsikan objek
class Mahasiswa {
  String nama;
  int usia;
}
 
 Mahasiswa(this.nama, this.usia);

  void study() {
    print('$nama sedang belajar.');
  }

// Fungsi asynchronous untuk mensimulasikan pengambilan data dari API
Future<String> fetchData() async {
  await Future.delayed(Duration(seconds: 2)); // Simulasi penundaan 2 detik
  return 'Data berhasil diambil!';
}

void main() async {
  // Membuat objek Mahasiswa
  Mahasiswa mahasiswa = Mahasiswa('John', 20);

  // Memanggil metode pada objek Mahasiswa
  mahasiswa.study();

  // Menjalankan operasi asynchronous
  print('Memulai pengambilan data...');
  String result = await fetchData();
  print(result);
  print('Pengambilan data selesai.');
}


