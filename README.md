
# Fuzzy Readiness Streamlit App

Di bawah ini **10 tahap lengkap** dari nol sampai deploy.

## 1) Siapkan folder proyek
```bash
mkdir fuzzy_streamlit_app && cd fuzzy_streamlit_app
```

## 2) (Opsional) Buat & aktifkan virtualenv
```bash
python -m venv .venv
# Windows
.venv\Scripts\activate
# macOS/Linux
source .venv/bin/activate
```

## 3) Salin berkas: `app.py`, `requirements.txt`, `sample_students.csv`
(Berkas sudah ada dalam ZIP ini.)

## 4) Instal dependensi
> Untuk Python 3.12, `scikit-fuzzy` harus dari GitHub (sudah tertulis di requirements).
```bash
pip install -U pip
pip install -r requirements.txt
```

## 5) Jalankan aplikasi lokal
```bash
streamlit run app.py
```

## 6) Uji input tunggal
- Atur slider **CGPA** dan **Exam** di sidebar.
- Klik **Hitung Readiness** → hasil crisp muncul.

## 7) Uji batch CSV
- Siapkan CSV dengan kolom `cgpa, exam` (case-insensitive).
- Unggah file → lihat tabel hasil → unduh CSV output.

## 8) Modifikasi membership function & rules (opsional)
- Edit bagian MF (`trimf/trapmf`) dan aturan di `app.py`.
- Simpan dan jalankan ulang.

## 9) Deploy ke Streamlit Community Cloud
1. Push ke GitHub.
2. Buka https://share.streamlit.io/ dan pilih repo kamu.
3. Set **Main file**: `app.py` → Deploy.

## 10) Troubleshooting anti-error
- **ModuleNotFoundError: imp** → pastikan `scikit-fuzzy` terpasang dari GitHub.
- **Build gagal** → Clear cache & redeploy.
- **CSV error** → pastikan kolom `cgpa` dan `exam` tersedia.
