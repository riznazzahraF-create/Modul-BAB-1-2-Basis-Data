# 📚 Rangkuman Modul Basis Data — BAB 1 & BAB 2
Dokumen ini merangkum konsep inti dari konversi ER ke model relasional serta pengantar Basis Data dan DDL.

---

## **🔷 BAB 1 — Konversi ER ke Tabel Relasional**

### **1. Entitas**
- **Entitas Kuat** → satu tabel; simple atribut → kolom; PK = atribut kunci.
- **Entitas Lemah** → tabel baru; PK = partial key + FK entitas kuat.

### **2. Atribut**
- **Komposit** → dipecah menjadi simple atribut.
- **Multinilai** → dibuat menjadi tabel tersendiri.
- **Turunan (Derived)** → opsional menjadi kolom.

### **3. Relasi**
- **1 : 1** → PK salah satu entitas menjadi FK di entitas lain.
- **1 : N** → PK entitas “1” menjadi FK di entitas “N”.
- **1 : N (dengan atribut relasi)** → dibuat tabel relasi khusus.
- **M : N** → harus dibuat tabel relasi baru berisi dua FK.
- **Unary** → satu tabel, tambahkan FK yang merujuk PK sendiri.
- **Ternary** → relasi menjadi tabel yang berisi semua FK.

### **4. Generalisasi & Spesialisasi (GENSPEC)**
- **Metode 1** → superclass & subclass masing-masing punya tabel.
- **Metode 2** → subclass menggabungkan atribut superclass + miliknya.

### **5. Agregasi**
- Relasi agregasi menghasilkan tabel berisi semua FK entitas yang terkait.

---

## **🧪 Studi Kasus Skema Apotek**
Entitas yang digunakan:
`pasien`, `dokter`, `resep`, `detail_resep`, `obat`,  
`kategori_obat`, `pegawai`, `pembayaran`.

---

## **🔷 BAB 2 — Pengantar Database & DDL**

### **1. DBMS**
Sistem untuk mengelola dan mengakses database. Contoh:
- MySQL
- PostgreSQL
- Oracle
- SQL Server

### **2. MySQL**
DBMS populer yang menggunakan bahasa SQL untuk mengelola data.

### **3. Cara Mengakses MySQL (XAMPP Terminal)**

```bash
cd C:\xampp\mysql\bin
mysql -u root -p

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
