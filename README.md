## 📝 Table of Contents

| No | Bagian       | Deskripsi                                                                 | Tautan |
|----|--------------|---------------------------------------------------------------------------|--------|
| 1  | **Pertemuan 1** | Penjelasan Bab 1 — *ERD* (Google Colab)                                    | 🔗 [Open Colab](https://colab.research.google.com/) |
| 2  | **Pertemuan 2** | Penjelasan Bab 2 — *Pengantar Basis Data & DDL* (Google Colab)            | 🔗 [Open Colab](https://colab.research.google.com/) |

# 📘 Rangkuman Modul Basis Data — BAB 1 & BAB 2
Rangkuman basis data yang fleksibel dan mudah untuk dipelajari 

---

## 🟦 BAB 1 — Konversi Entity Relationship (ER)

### 🔹 1. Entitas Kuat (Strong Entity)
- Setiap entitas kuat → **1 tabel**
- Setiap atribut sederhana → **kolom**
- Atribut kunci → **PRIMARY KEY**

> **Entitas → Tabel**  
> **Atribut → Kolom**

---

### 🔹 2. Atribut Komposit (Composite Attribute)
- Tabel tetap mengikuti entitas kuat.  
- **Atribut komposit tidak dibuat kolom langsung** (misal: alamat → pecah menjadi jalan, kota, kode_pos).

---

### 🔹 3. Atribut Multivalue (Multivalue Attribute)
- Harus dibuat menjadi **tabel baru**  
- Akibatnya entitas yang memiliki atribut multivalue → menjadi **2 tabel**

---

### 🔹 4. Atribut Turunan (Derived Attribute)
- Bisa dibuat sebagai kolom bila dibutuhkan (opsional).

---

### 🔹 5. Entitas Lemah (Weak Entity)
- Menjadi **tabel sendiri**  
- Atribut sederhana → kolom  
- Memiliki **partial key + foreign key** dari entitas kuat

---

### 🔹 6. Relasi One-to-One
- Primary key salah satu entitas → menjadi **FOREIGN KEY** pada entitas lainnya.

---

### 🔹 7. Relasi One-to-Many
- Primary key dari sisi **One** → menjadi **FOREIGN KEY** pada sisi **Many**

---

### 🔹 8. One-to-Many (Relasi memiliki atribut)
- Dibuat **3 tabel**:
  1. Tabel entitas 1  
  2. Tabel entitas 2  
  3. Tabel relasi (berisi FK + atribut relasinya)

---

### 🔹 9. Relasi Many-to-Many
- Dibuat menjadi **tabel relasi**
- Simple atribut di relasi → kolom
- Foreign key berasal dari kedua entitas

---

### 🔹 10. Relasi Unary (Recursive)
- Kolom PK tetap  
- Ditambahkan kolom FK yang merujuk *ke tabel yang sama*
- Tabel yang terbentuk hanya **1 tabel**

---

### 🔹 11. Relasi Ternary
- Relasi tiga entitas → **1 tabel relasi**
- Simple atribut → kolom  
- Setiap entitas menyumbang **foreign key**

---

### 🔹 12. Generalisasi & Spesialisasi (GENSPEC)
#### ✔ Metode 1 (Super → Sub)
- Superclass = tabel (PK + simple atribut)  
- Subclass = tabel, mewarisi PK dari superclass sebagai **PRIMARY KEY**

#### ✔ Metode 2 (Full Copy)
- Subclass = tabel  
- Atribut superclass ikut dipindah ke subclass  
- PK superclass → PK subclass

---

### 🔹 13. Agregasi
- PK entitas agregasi → PK tabel  
- Relasi dengan entitas lain menggunakan kombinasi **foreign key** dari entitas yang terlibat agregasi.

---

## 🏥 Studi Kasus: Skema Pembayaran Apotek
Terdiri dari tabel:
1. pasien  
2. dokter  
3. resep  
4. detail_resep  
5. obat  
6. kategori_obat  
7. pegawai  
8. pembayaran  

---

# 🟩 BAB 2 — Pengantar Basis Data & DDL

### 🔹 DBMS (Database Management System)
Sistem yang digunakan untuk mengelola database.  
Contoh: **MySQL**, Oracle, PostgreSQL, SQL Server, dll.

### 🔹 MySQL (My Structured Query Language)
Salah satu DBMS populer dan gratis, sering digunakan pada aplikasi web.

---

## 🔧 Cara Mengakses MySQL

### **1. Masuk ke folder MySQL**
```bash
cd C:\xampp\mysql\bin
mysql -u root -p
