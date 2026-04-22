# 🎨 Renk Düzenleme (Color Grading)

> Gözleriniz sizi yanıltabilir, matematik ve araçlar (scopes) asla. Renk, hikaye anlatımının en güçlü bilinçaltı aracıdır.

---

## 📽️ Format Farkları: RAW, LOG ve Rec.709

| Format | Dinamik Aralık | Esneklik | İşlem Gücü |
|--------|----------------|----------|------------|
| **Rec.709** | Düşük (Kısıtlı) | Çok Az | Çok Düşük (Hafif) |
| **LOG** | Çok Yüksek | Yüksek | Orta |
| **RAW** | Maksimum | Sınırsız (ISO/WB değişebilir) | Çok Yüksek (Ağır) |

---

## 🏗️ Renk Yönetimi (Color Management)

Profesyonel iş akışlarında "göz kararı" renk yapmak yerine bir sistem kullanılır.

### ACES (Academy Color Encoding System)
Renklerin farklı kameralar ve ekranlar arasında tutarlı görünmesini sağlayan endüstri standardıdır.
- **IDT (Input):** Kameranın renk profilini ACES uzayına çevirir.
- **ODT (Output):** ACES uzayındaki görüntüyü izleyicinin ekranına (Rec.709, HDR vb.) çevirir.

---

## 🔑 İki Temel Safha

### 1. Color Correction (Renk Doğrulama)
**Teknik** süreçtir. Görüntüyü "sıfır" noktasına getirmektir.
- White Balance & Exposure düzeltme.
- Kamera eşleme (Match Shot).
- **Signal Chain:** Correction her zaman Grading'den önce gelmelidir.

### 2. Color Grading (Derecelendirme)
**Sanat** ve **Psikoloji**. İzleyiciye ne hissettirmek istiyorsunuz?
- **Primary Grading:** Tüm görüntüyü etkileyen genel değişiklikler.
- **Secondary Grading:** Sadece belirli bir bölgeyi (örn: gökyüzünün mavisi) veya rengi (örn: sadece kırmızı elbise) değiştirme.
- **Power Windows & Tracking:** Hareketli bir nesneyi maskeleyerek sadece ona müdahale etme.

---

## 📊 Renk Araçları (Scopes)

| Scope | Görevi | Kritik Nokta |
|-------|--------|---------------|
| **Waveform** | Parlaklık (Luma) | 0 (Siyah) - 100/1023 (Beyaz) arası. |
| **Parade** | RGB Dengesi | Kanalların alt/üst sınırları dengeli olmalı. |
| **Vectorscope** | Ton ve Doygunluk | **Skin Tone Line:** İnsan cildi bu çizgi üzerindedir. |

---

## 🔄 CST (Color Space Transform) vs. LUT

Profesyonel renkçiler artık Log → Rec.709 dönüşümü için LUT yerine **CST** kullanmaktadır.

- **CST:** Matematikseldir. Veriyi bozmadan (clipping yapmadan) renk uzayları arası geçiş yapar.
- **LUT:** Sabit bir "filtre" gibidir. Pozlamanız LUT'a tam uygun değilse detay kaybı yaşatabilir.

---

## 🌈 Renk Teorisi ve Psikoloji

*   **Complementary (Karşıt):** Orange & Teal. Derinlik ve kontrast sağlar.
*   **Analogous (Benzer):** Yeşil ve Sarı tonlar. Huzur ve bütünlük sağlar.
*   **Triadic:** Üç farklı canlı renk. Enerji ve çocuksu bir hava verir.

**Duygusal Karşılıklar:**
- **Sıcak:** Samimiyet, enerji, geçmişe özlem.
- **Soğuk:** Mesafe, teknoloji, korku, gelecek.

---

## 🛠️ Popüler Renk Yazılımları

1.  **DaVinci Resolve:** Sektör standardı, düğüm (node) tabanlı çalışma.
2.  **Adobe Premiere Pro (Lumetri):** Katman tabanlı, hızlı ve pratik.
3.  **Color Finale / FCPX:** Mac kullanıcıları için optimize.

---

[🏠 README'ye Dön](../README.md)
