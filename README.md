# 🗺️ GeoJSON Sulawesi Barat (Sulbar)

![Data Badge](https://img.shields.io/badge/Data-GeoJSON-orange?style=for-the-badge&logo=json)
![Location](https://img.shields.io/badge/Region-West%20Sulawesi-blue?style=for-the-badge&logo=openstreetmap)
![License](https://img.shields.io/badge/License-Open%20Source-green?style=for-the-badge)

Repositori ini berisi kumpulan data spasial (peta digital) provinsi **Sulawesi Barat** dalam format **GeoJSON**. Data ini dapat digunakan untuk keperluan pembuatan aplikasi GIS (Geographic Information System), visualisasi data, atau penelitian akademis.

## 📂 Daftar Wilayah
Data yang tersedia mencakup batas administrasi untuk Kabupaten/Kota di Sulawesi Barat:

| No | Nama File | Wilayah (Kabupaten) |
| :--- | :--- | :--- |
| 1. | `majene.geojson` | 📍 Kab. Majene |
| 2. | `mamuju.geojson` | 📍 Kab. Mamuju (Ibukota) |
| 3. | `polman.geojson` | 📍 Kab. Polewali Mandar |
| 4. | `mamasa.geojson` | 📍 Kab. Mamasa |
| 5. | `pasangkayu.geojson` | 📍 Kab. Pasangkayu |
| 6. | `mateng.geojson` | 📍 Kab. Mamuju Tengah |
| 7. | `sulbar_full.geojson` | 🗺️ Provinsi Sulawesi Barat (Gabungan) |

*(Pastikan nama file di atas sesuai dengan yang ada di repo Anda, jika berbeda silakan disesuaikan)*

## 🚀 Cara Penggunaan

### 1. Menggunakan Leaflet.js (Web)
Jika Anda membangun web GIS, Anda bisa langsung memuat file ini menggunakan `fetch` atau AJAX.

```javascript
// Contoh memuat peta Majene
fetch('[https://raw.githubusercontent.com/Zaammm16/GeoJson_Sulbar/main/majene.geojson](https://raw.githubusercontent.com/Zaammm16/GeoJson_Sulbar/main/majene.geojson)')
  .then(response => response.json())
  .then(data => {
    L.geoJSON(data, {
      style: { color: "#ff7800", weight: 2 }
    }).addTo(map);
  });
