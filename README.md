# Rangkuman Modul Basis Data — BAB 1 & 2
Ringkasan untuk Basis Data pada BAB 1 & 2 supaya mudah untuk dipahami dan dicerna.

---

## 📘 BAB 1 — Konversi ER ke Model Relasional

### 1. Entitas Kuat
- Setiap entitas kuat menjadi **1 tabel**.
- Simple atribut → kolom.
- Atribut kunci → **Primary Key**.

### 2. Composite Atribut
- Tidak jadi kolom langsung.
- Dipecah menjadi simple atribut.

### 3. Multivalue Atribut
- Dibuat menjadi **tabel baru**.
- Berisi FK + nilai atribut.

### 4. Derived Atribut
- Boleh dijadikan kolom, namun biasanya dihitung dari atribut lain.

### 5. Entitas Lemah
- Menjadi tabel.
- PK = Partial key + FK dari entitas kuat.

### 6. Relasi One-to-One (1:1)
- PK salah satu entitas menjadi FK di entitas lainnya.

### 7. Relasi One-to-Many (1:N)
- PK entitas "One" menjadi FK di entitas "Many".

### 8. One-to-Many dengan Atribut Relasi
- Dibuat **3 tabel**: entitas 1, entitas 2, tabel relasi.

### 9. Many-to-Many (M:N)
- Dibuat tabel relasi baru.
- Berisi FK dari kedua entitas + atribut relasi.

### 10. Unary Relationship
- Tetap 1 tabel.
- Menambah FK yang merujuk PK tabel sendiri.

### 11. Ternary Relationship
- Dibuat tabel relasi berisi semua FK + atribut relasi.

### 12. GENSPEC (Generalization & Specialization)
**Metode 1**  
- Superclass → tabel  
- Subclass → tabel, PK superclass menjadi PK subclass  

**Metode 2**  
- Subclass → tabel dengan seluruh atribut superclass  

### 13. Agregasi
- Tabel relasi berisi FK dari semua entitas yang berpartisipasi.

---

## 📚 Studi Kasus: Skema Pembayaran Apotek
Entitas yang terlibat:
- pasien
- dokter
- resep
- detail_resep
- obat
- kategori_obat
- pegawai
- pembayaran

---

## 📘 BAB 2 — Pengantar Basis Data & DDL

### 1. DBMS
Sistem untuk mengelola database, contoh:
- MySQL
- Oracle
- PostgreSQL
- SQL Server

### 2. MySQL
Salah satu DBMS populer yang menggunakan SQL sebagai bahasa utama.

### 3. Akses MySQL (via XAMPP Terminal)

```bash
cd C:\xampp\mysql\bin
mysql -u root -p
