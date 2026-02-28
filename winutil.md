# [🔐 Cara Aman Install WinUtil (Direkomendasikan)](https://chatgpt.com/s/t_69a33c284c848191bf0ac1e2bf51f548)

Daripada menjalankan langsung `irm | iex`, lebih aman **download script terlebih dahulu** lalu jalankan dari file lokal.

---

## 1️⃣ Download Script WinUtil

Buka **PowerShell 7** (Run as Administrator), Masuk ke folder C:\Windows\System32 (bypass the Constrained Language Mode), lalu jalankan:

```powershell
Invoke-WebRequest https://christitus.com/win -OutFile winutil.ps1
```

File akan tersimpan di folder yang dipilih (misal `System32`).

---

## 2️⃣ (Opsional) Cek Isi Script

Sebelum menjalankan, disarankan untuk melihat isi script supaya tahu tweak apa yang dijalankan:

```powershell
notepad .\winutil.ps1
```

> Ini langkah keamanan: memastikan script dari sumber resmi dan tidak mengandung hal berbahaya.

---

## 3️⃣ Jalankan WinUtil

Setelah dicek, jalankan script lokal:

```powershell
.\winutil.ps1
```

WinUtil akan terbuka, siap digunakan.

# [Full Guide](https://chatgpt.com/s/t_69a33f11de348191ab91bf222a3e2993)

## 🟢 STEP 1 — Buka PowerShell 7

1. Klik **Start**
2. Ketik **PowerShell 7**
3. Klik kanan → **Run as Administrator**

---

## 🟢 STEP 2 — Masuk ke Folder Tempat Simpan

Contoh kita simpan di **System32** (bypass the Constrained Language Mode):

```powershell
cd $env:USERPROFILE\Downloads
```

> Ganti path sesuai foldermu jika berbeda.

---

## 🟢 STEP 3 — Download / Install WinUtil Pertama Kali

```powershell
Invoke-WebRequest https://christitus.com/win -OutFile winutil.ps1
```

✅ Akan membuat file `winutil.ps1` baru atau menimpa versi lama jika sudah ada.

---

## 🟢 STEP 4 — (Opsional) Buka Isi WinUtil Sebelum Dijalankan

```powershell
notepad .\winutil.ps1
```

> Langkah ini opsional tapi disarankan untuk memastikan script yang akan dijalankan berasal dari sumber resmi.

---

## 🟢 STEP 5 — Unblock File

```powershell
Unblock-File .\winutil.ps1
```

---

## 🟢 STEP 6 — Jalankan WinUtil

```powershell
.\winutil.ps1
```

✅ WinUtil akan terbuka.

---

## 🟢 STEP 7 — Menutup WinUtil

Tutup WinUtil seperti aplikasi biasa setelah selesai melakukan tweak.

---

## 🟢 STEP 8 — Membuka Ulang WinUtil

Kalau ingin membuka lagi tanpa download ulang:

1. Buka PowerShell 7 (Admin)
2. Masuk folder tempat file disimpan:

```powershell
cd C:\Windows\System32
```

3. Jalankan:

```powershell
.\winutil.ps1
```

✅ WinUtil akan terbuka kembali.

---

## 🟢 STEP 9 — Update WinUtil ke Versi Terbaru (1 Baris Super Singkat)

Gunakan 1 baris ini untuk **update + unblock + buka sekaligus**:

```powershell
cd C:\Windows\System32; Invoke-WebRequest https://christitus.com/win -OutFile winutil.ps1; Unblock-File .\winutil.ps1; .\winutil.ps1
```

### Penjelasan:

1. Masuk ke folder tempat WinUtil disimpan
2. Download versi terbaru (atau menimpa versi lama)
3. Unblock file agar tidak diblokir Windows
4. Jalankan WinUtil langsung

