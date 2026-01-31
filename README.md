# TextLoco - Halu Generator

Proyek ini adalah generator copypasta "halu" yang menggunakan template YAML dan frontend HTML.

## Prasyarat

- Python 3
- PyYAML

## Cara Menjalankan

### 1. Install Dependensi
Buka terminal di folder proyek ini dan jalankan:
```bash
pip install PyYAML
```

### 2. Generate Data Copypasta
Jalankan script Python untuk menggabungkan semua template YAML menjadi satu file JSON:
```bash
python generate_copypasta.py
```
Perintah ini akan menghasilkan file `copypasta.json`.

### 3. Jalankan Server Lokal
Karena file HTML mengambil data dari `copypasta.json` menggunakan `fetch`, Anda perlu menjalankan server lokal:
```bash
python -m http.server
```

### 4. Buka di Browser
Buka browser dan akses:
[http://localhost:8000](http://localhost:8000)

## Struktur Proyek
- `copypasta/`: Berisi template copypasta dalam format YAML.
- `generate_copypasta.py`: Script untuk mengkonversi YAML ke JSON.
- `index.html`: Antarmuka pengguna (frontend).
- `write_commit.py`: Digunakan untuk CI/CD (menambahkan hash commit ke footer).
