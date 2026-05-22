\# API Testing Results - JSONPlaceholder API



\*\*Tester:\*\* Balqis Naurah Hanifah  

\*\*API Base URL:\*\* https://jsonplaceholder.typicode.com  

\*\*Tool:\*\* Postman  

\*\*Tanggal:\*\* 2026-05-10  



\---



\## Ringkasan Pengujian



| No | Endpoint | Method | Deskripsi | Status Code | Hasil |

|----|----------|--------|-----------|-------------|-------|

| 1 | /users | GET | Mengambil daftar user | 200 | PASS |

| 2 | /users/1 | GET | Mengambil detail user | 200 | PASS |

| 3 | /users/999 | GET | User tidak ditemukan | 404 | PASS |

| 4 | /users | POST | Membuat user baru | 201 | PASS |

| 5 | /users/1 | PUT | Mengupdate data user | 200 | PASS |

| 6 | /users/1 | DELETE | Menghapus user | 200 | PASS |

| 7 | /posts | GET | Mengambil semua posts | 200 | PASS |

| 8 | /posts/1/comments | GET | Komentar dari post tertentu | 200 | PASS |



\---



\## Detail Validasi



\### GET /users

\- Response status 200

\- Data berupa array dengan 10 elemen

\- Setiap user memiliki field: id, name, email, username



\### GET /users/1

\- Response status 200

\- ID user sesuai dengan yang diminta (1)

\- Format email valid



\### GET /users/999

\- Response status 404

\- User tidak ditemukan, error handling sudah benar



\### POST /users

\- Response status 201

\- Response mengandung data yang dikirim (name, email)

\- Response memiliki field id (auto-generated)



\### PUT /users/1

\- Response status 200

\- Response mencerminkan data yang diupdate



\### DELETE /users/1

\- Response status 200

\- User berhasil dihapus



\### GET /posts

\- Response status 200

\- Returns 100 posts

\- Setiap post memiliki field title dan body



\### GET /posts/1/comments

\- Response status 200

\- Setiap comment memiliki postId = 1



\---



\## Total



| Metrik | Nilai |

|--------|-------|

| Total Test Case | 8 |

| Pass | 8 |

| Fail | 0 |

| Pass Rate | 100% |

