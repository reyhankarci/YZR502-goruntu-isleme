# YZR502 — Görüntü İşleme Ödevi
## Robotik Görüde Parametre Analizi: Kenar Tespiti, Kontur Bulma ve ORB Öznitelik Çıkarma

---

## Öğrenci Bilgileri
- **Ad Soyad:** Reyhan Karcı
- **Öğrenci No:** 25680101
- **Ders:** YZR502 Robotik Sistemler ve Algoritmalar
- **YouTube:** []

---

## Proje Açıklaması
Bu çalışmada bir robotik görü senaryosu üzerinden görüntü işleme hattı uygulanmıştır.
Gauss yumuşatma, CLAHE kontrast iyileştirme, Canny kenar tespiti ve ORB öznitelik
çıkarma adımlarından oluşan pipeline, farklı parametre setleriyle test edilmiştir.

---

## Deney Konfigürasyonları ve Sonuçlar

| Deney | gaussian_sigma | clahe_clip | canny_low | canny_high | Toplam Kontur | Geçerli Kontur | ORB Nokta | Ort. Dairesellik | Ort. Alan |
|-------|---------------|------------|-----------|------------|---------------|----------------|-----------|------------------|-----------|
| Deney 1 (Varsayılan) | 1.5 | 2.0 | 50 | 150 | 334 | 2 | 500 | 0.010 | 839.8 |
| Deney 2 (Agresif Kenar) | 1.5 | 2.0 | 30 | 90 | 612 | 2 | 500 | 0.010 | 839.8 |
| Deney 3 (Güçlü Yumuşatma) | 3.0 | 2.0 | 50 | 150 | 316 | 0 | 500 | 0.000 | 0.0 |

---

## Deney Görselleri

### Deney 1 — Varsayılan
![Deney 1](Deney_1_(Varsayılan).png)

### Deney 2 — Agresif Kenar Tespiti
![Deney 2](Deney_2_(Agresif_Kenar_Tespiti).png)

### Deney 3 — Güçlü Yumuşatma
![Deney 3](Deney_3_(Güçlü_Yumuşatma).png)

---

## Kullanılan Teknolojiler
- Python 3
- OpenCV
- NumPy
- Matplotlib
- Google Colab

---

## Dosya Yapısı
```
├── goruntu_isleme_odevi.ipynb   # Tamamlanmış Colab notebook
├── Deney_1_(Varsayılan).png     # Deney 1 çıktı görseli
├── Deney_2_(Agresif_Kenar_Tespiti).png  # Deney 2 çıktı görseli
├── Deney_3_(Güçlü_Yumuşatma).png       # Deney 3 çıktı görseli
└── README.md
```
