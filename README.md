# 📘 Rangkuman Modul Basis Data — BAB 1 dan BAB 2
rangkuman materi Basis Data supaya mudah dipahami dan dipelajari
---

## 🔹 BAB 1 — Konversi ER ke Model Relasional

### **1. Entitas**
- **Entitas Kuat** → menjadi satu tabel lengkap berisi seluruh simple atribut dengan primary key sebagai identitas unik.  
- **Entitas Lemah** → dibentuk tabel baru dengan primary key gabungan (partial key + foreign key dari entitas kuat).

### **2. Atribut**
- **Komposit** → dipecah menjadi beberapa simple atribut.  
- **Multinilai** → dipisahkan ke dalam tabel khusus berisi foreign key + nilai atribut.  
- **Turunan (Derived)** → dapat ditambahkan sebagai kolom jika diperlukan untuk efisiensi pemrosesan data.

### **3. Relasi Antar Entitas**
- **One-to-One (1:1)** → salah satu tabel menyimpan FK dari tabel lainnya.  
- **One-to-Many (1:N)** → entitas “Many” menyimpan FK dari entitas “One”.  
- **One-to-Many dengan atribut relasi** → hubungan dibuat dalam tabel relasi terpisah.  
- **Many-to-Many (M:N)** → dibentuk tabel relasi baru berisi FK dari kedua entitas.  
- **Unary Relationship** → satu tabel dengan FK yang merujuk PK tabel sendiri.  
- **Ternary** → satu tabel relasi memuat seluruh FK dari tiga entitas.

### **4. Generalisasi & Spesialisasi (GENSPEC)**
- **Metode 1** → superclass & subclass masing-masing memiliki tabel; PK superclass diwariskan ke subclass.  
- **Metode 2** → subclass menggabungkan atribut superclass + atribut miliknya ke dalam satu tabel.

### **5. Agregasi**
- Produksi tabel relasi yang memuat semua foreign key dari entitas yang terlibat dalam proses agregasi.

---

## 📌 Studi Kasus: Skema Pembayaran Apotek
Entitas yang digunakan:
- `pasien`
- `dokter`
- `resep`
- `detail_resep`
- `obat`
- `kategori_obat`
- `pegawai`
- `pembayaran`

---

## 🔹 BAB 2 — Pengantar Basis Data & DDL

### **1. DBMS**
Perangkat lunak untuk mengelola database, termasuk penyimpanan, pengolahan, dan pengamanan data.

### **2. MySQL**
Salah satu DBMS yang paling banyak digunakan, mendukung operasi dasar SQL seperti pembuatan tabel, manipulasi data, dan kontrol akses.

### **3. Mengakses MySQL (XAMPP)**
Gunakan terminal untuk masuk ke MySQL:

```bash
cd C:\xampp\mysql\bin
mysql -u root -p
