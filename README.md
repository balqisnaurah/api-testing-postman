# API Testing dengan Postman

Pengujian API menggunakan Postman dengan automated test scripts. Mencakup 8 endpoint dari JSONPlaceholder API yang mengilustrasikan operasi CRUD lengkap dan validasi response.

---

## Daftar File

### `Reqres_API_Testing.postman_collection.json`

Postman collection yang berisi 8 request beserta automated test scripts. Bisa di-import langsung ke Postman untuk dijalankan.

**Daftar Request:**

| No | Request | Method | Endpoint | Status Code |
|----|---------|--------|----------|-------------|
| 1 | GET List Users | GET | /users | 200 |
| 2 | Get Single User | GET | /users/1 | 200 |
| 3 | Get User Not Found | GET | /users/999 | 404 |
| 4 | Create User | POST | /users | 201 |
| 5 | Update User | PUT | /users/1 | 200 |
| 6 | Delete User | DELETE | /users/1 | 200 |
| 7 | Get All Posts | GET | /posts | 200 |
| 8 | Get Comments by Post | GET | /posts/1/comments | 200 |

---

### `API_TEST_RESULTS.md`

Dokumentasi hasil pengujian API yang merangkum:
- Tabel ringkasan semua endpoint yang diuji
- Detail validasi untuk setiap endpoint
- Status pass/fail dan total pass rate

---

## Jenis Validasi yang Dilakukan

Untuk setiap endpoint, dilakukan validasi:

| Validasi | Deskripsi |
|----------|-----------|
| **Status Code** | Memastikan response code sesuai (200, 201, 404, dll) |
| **Response Structure** | Memvalidasi struktur JSON response |
| **Required Fields** | Memastikan field-field penting ada di response |
| **Data Type** | Memvalidasi tipe data (string, number, array) |
| **Data Integrity** | Memastikan data yang dikirim = data yang dikembalikan |
| **Error Handling** | Memvalidasi response untuk error case (404) |

---

## API yang Diuji

**Base URL:** https://jsonplaceholder.typicode.com

JSONPlaceholder adalah free fake REST API yang umum digunakan untuk testing dan prototyping.

---

## Cara Menggunakan

1. Buka Postman
2. Klik **Import** di kiri atas
3. Pilih file `Reqres_API_Testing.postman_collection.json`
4. Collection akan muncul di sidebar
5. Klik kanan collection → **Run collection** untuk menjalankan semua request

Atau jalankan request satu per satu untuk melihat detail response dan hasil test.

---

## Hasil Akhir

| Metrik | Nilai |
|--------|-------|
| Total Test Case | 8 |
| Pass | 8 |
| Fail | 0 |
| Pass Rate | 100% |

---

## Tentang

Proyek ini dibuat sebagai bagian dari proses belajar Quality Assurance, khususnya dalam API testing menggunakan Postman. Setiap request dilengkapi dengan automated test scripts dalam JavaScript untuk memvalidasi response secara otomatis. Tools dan teknik yang digunakan adalah praktik standar industri yang umum diterapkan di tim QA.
