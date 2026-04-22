# 📤 Dışa Aktarma ve Codec'ler

> Yanlış export ayarı, haftalarca süren kurgu ve renk emeğini bir anda çöpe atabilir. Kalite ile dosya boyutu arasındaki dengeyi kurmak teknik bir sanattır.

---

## 🔑 Temel Kavramlar

### Codec vs. Container (Kapsayıcı)
- **Container (.mp4, .mov, .mxf):** İçinde video, ses ve metadata barındıran "kutu".
- **Codec (H.264, ProRes, AV1):** Görüntü verisini sıkıştıran ve açan matematiksel yöntem.

- **4:4:4:** Renk verisi %100 korunur. (VFX, Master arşiv).

### 💎 Bit-Derinliği (Bit-Depth)
Görüntüdeki renk geçişlerinin (gradient) pürüzsüzlüğünü belirler.
- **8-bit:** 16.7 milyon renk. Gökyüzü gibi alanlarda "banding" (renk kırılması) yapabilir.
- **10-bit:** 1.07 milyar renk. Profesyonel renk düzenleme ve HDR için zorunludur.
- **12-bit:** 68.7 milyar renk. Sinema kameraları (RAW) için standarttır.

---

## 🔝 Mezzanine (Ara) Formatlar
Kurgu bittikten sonra, renk veya VFX için gönderilen yüksek kaliteli formatlardır.

| Format | Codec | Özellik |
|--------|-------|---------|
| **Apple ProRes 422 HQ** | 10-bit | Genel profesyonel standart. |
| **ProRes 4444 / XQ** | 12-bit | Yüksek dinamik aralık ve Alpha (şeffaflık) desteği. |
| **Avid DNxHR** | 10-bit | Windows/PC ekosistemi için en iyi performans. |
| **GoPro CineForm** | 10-bit | Kayıpsıza yakın, çok hızlı işleme. |

---

## 🏗️ Profesyonel Teslimat (Mastering)

Sadece YouTube için değil, farklı mecralar için "Master" paketler hazırlanır:

| Teslimat Türü | Format | Kullanım Alanı |
|---------------|--------|----------------|
| **DCP (Digital Cinema Package)** | MXF (JPEG 2000) | Sinema salonları için şifreli paket. |
| **IMF (Interoperable Master Format)** | MXF | Netflix, Amazon gibi büyük yayın ağları için yüksek kaliteli kaynak dosya. |
| **ProRes 4444 / HQ** | .MOV | Arşivleme ve daha sonraki düzenlemeler için en yüksek kalite. |

---

## 📊 Bitrate Hesaplama ve Dosya Boyutu

Dosya boyutu, çözünürlükten ziyade **Bitrate** (Bit hızı) ile ilgilidir.
- **VBR (Variable Bit Rate):** Aksiyonun olduğu yerde bitrate'i artırır, sakin yerde düşürür. (Daha verimli).
- **CBR (Constant Bit Rate):** Her zaman aynı hız. (Canlı yayınlar için uygun).

**Formül:** `Dosya Boyutu (MB) = [Bitrate (Mbps) x Süre (Saniye)] / 8`
*Örn: 10 Mbps ile 60 saniyelik bir video = 600 / 8 = 75 MB.*

---

## 📱 Sosyal Medya Optimizasyonu (YouTube, TikTok, Instagram)

Her platform videonuzu tekrar sıkıştırır. Bu kaybı en aza indirmek için:

| Platform | Format | Çözünürlük | Önerilen Bitrate (H.264) |
|----------|--------|------------|---------------------------|
| **YouTube (4K)** | MP4 | 3840x2160 | 45-60 Mbps |
| **Instagram Reels** | MP4 | 1080x1920 (9:16) | 15 Mbps |
| **TikTok** | MP4 | 1080x1920 | 10-15 Mbps |

---

## 📺 HDR (High Dynamic Range) Export

HDR video, standart (SDR) videolara göre çok daha fazla parlaklık ve renk bilgisi taşır.
- **Rec.2020:** HDR için kullanılan geniş renk uzayı.
- **Nits:** Parlaklık birimi. HDR10 için genellikle 1000 nits hedef alınır.

---

## 🛠️ Teknik Terimler ve Dipnotlar

*   **Alpha Channel:** Görselin şeffaflık bilgisi (Logo veya alt yazı export alırken ProRes 4444 kullanılır).
*   **Frame Rate (Kare Hızı):** 24 fps (Sinematik), 30 fps (TV/Vlog), 60 fps (Oyun/Spor).
*   **Multiplexer:** MP4 veya MOV gibi konteyneri oluşturan yapı.

---

## 🌈 HDR (High Dynamic Range) Export

Geleneksel Rec.709 (SDR) dışına çıkmak için:
- **Renk Uzayı:** Rec.2020.
- **Aktarım Fonksiyonu (EOTF):** ST.2084 (PQ) veya HLG.
- **Metadata:** YouTube veya TV platformlarının HDR'ı tanıması için master metadata bilgilerini (MaxCLL, MaxFALL) exporta ekleyin.

---

## 🖥️ Interlaced vs. Progressive

Modern dünyada **Progressive (p)** kuraldır.
- **Progressive (1080p):** Satırlar sırayla çizilir. Net ve keskin.
- **Interlaced (1080i):** Önce tek, sonra çift satırlar çizilir. Hareketli sahnelerde "taraklanma" (combing) yapar. Sadece eski TV yayın standartları zorunlu tutarsa kullanın.

---

1.  **YouTube:** H.264 yerine mümkünse **H.265 (HEVC)** kullanın. Daha küçük boyutta daha fazla detay (özellikle 4K'da) sağlar.
2.  **Instagram & TikTok:**
    | Platform | Oran | Çözünürlük | FPS | Bitrate |
    | :--- | :--- | :--- | :--- | :--- |
    | **Reels/TikTok** | 9:16 | 1080x1920 | 30/60 | 10-15 Mbps |
    | **YouTube HD** | 16:9 | 1920x1080 | 24/25 | 8-12 Mbps |
3.  **WhatsApp/Telegram:** Göndermeden önce çözünürlüğü 720p'ye düşürmek, izleyici deneyimini hızlandırır.

---

## 🏛️ Arşivleme: Gold Master ve LTO

İş bittiğinde sadece "Final.mp4" almak yeterli değildir:
- **Gold Master:** Hiçbir yazı veya grafik içermeyen (Clean), en yüksek kaliteli (ProRes 4444) ana kopya.
- **Project Managed Archive:** Sadece kullanılan kliplerin ve proje dosyasının saklandığı paket.
- **LTO (Linear Tape-Open):** Uzun vadeli (30+ yıl) saklama için kullanılan manyetik bant yedekleme sistemi.

---

[🏠 README'ye Dön](../README.md)
