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

---

## 🏗️ Renk Yönetimi (Color Management)

Profesyonel iş akışlarında "göz kararı" renk yapmak yerine matematiksel bir sistem kullanılır.

### ACES (Academy Color Encoding System)
Farklı kameralar (Sony, RED, Arri) arasındaki renk farklarını eşitleyen evrensel standart.
- **IDT:** Kameranın RAW/Log verisini ACES uzayına taşır.
- **ODT:** Projeyi izleyici ekranına (Rec.709, HDR) uygun hale getirir.

---

## 🎨 Teknik Detaylar: Bit Derinliği ve Subsampling

Renkçinin en büyük düşmanı **banding** (renk geçişlerinde oluşan artifactlar) ve **noise**'dur.

| Özellik | Detay | Önemi |
|---------|-------|-------|
| **Bit Depth** | **8-bit** (256 değer) vs **10-bit** (1024 değer) | 10-bit, renk düzenlemede (özellikle gökyüzü gibi yumuşak geçişlerde) parçalanmayı önler. |
| **Chroma Subsampling** | **4:2:0** vs **4:2:2** vs **4:4:4** | Yeşil perde (Chroma Key) işlerinde 4:2:2 ve üzeri net kenarlar için şarttır. |

---

## 🏗️ DaVinci Resolve: Nodal Yapı (Node Strategy)

Renk düzenleme katmanlar yerine düğümler (nodes) üzerinden ilerler. Tipik bir **Fixed Node Tree**:
1.  **Noise Reduction:** (Eğer gerekiyorsa) İlk sırada yapılır.
2.  **Exposure / WB:** Pozlama ve beyaz dengesini "sıfırlama".
3.  **CST (Color Space Transform):** Log görüntüyü Rec.709'a çevirme.
4.  **Match Shots:** Sahneler arası tutarlılık sağlama.
5.  **Look Dev:** Filmin sanatsal tonunu (Teal & Orange vb.) verme.
6.  **Film Grain:** Dokusal derinlik için film greni ekleme.

---

## 📊 Renk Araçları (Scopes)

| Scope | Kritik Nokta |
|-------|---------------|
| **Waveform** | 0-100 IRE arası. 100'ün üzeri "patlar", 0'ın altı "bilgi kaybıdır". |
| **Vectorscope** | **Skin Tone Line:** İnsan cildi (ırk fark etmeksizin) bu çizgi üzerine düşmelidir. |
| **Parade** | Kırmızı, Yeşil ve Mavi kanalların dengesi. Beyaz dengesi için en iyi araçtır. |

---

## 🔄 CST (Color Space Transform) vs. LUT

- **CST:** Matematikseldir. Veriyi bozmadan dönüştürür. Dinamik aralığı korur.
- **LUT:** Sabit bir "maske" gibidir. Pozlamanız LUT'a tam doğru değilse veriyi kalıcı olarak siyah/beyazda ezebilir (clipping).

---

## 🌈 Look Development (Görünüm Tasarımı)

Renk düzenleme sadece düzeltme değil, bir **atmosfer** yaratmaktır.
- **Kodak/Fuji Emulation:** Dijital görüntüyü analog film gibi hissettirme.
- **Power Windows & Tracking:** Hareketli bir karakteri aydınlatıp arka planı karartarak odağı yönetme.
- **Color Contrast:** Sadece parlaklık ile değil, zıt renkler (Mavi - Turuncu gibi) ile derinlik yaratma.

---

## 🛠️ Popüler Renk Yazılımları

1.  **DaVinci Resolve:** Sektör standardı, düğüm (node) tabanlı çalışma.
2.  **Adobe Premiere Pro (Lumetri):** Katman tabanlı, hızlı ve pratik.
3.  **Color Finale / FCPX:** Mac kullanıcıları için optimize.

---

[🏠 README'ye Dön](../README.md)
