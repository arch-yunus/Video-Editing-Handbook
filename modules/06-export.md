# 📤 Dışa Aktarma ve Codec'ler

> Yanlış export ayarı, haftalarca süren kurgu ve renk emeğini bir anda çöpe atabilir. Kalite ile dosya boyutu arasındaki dengeyi kurmak teknik bir sanattır.

---

## 🔑 Temel Kavramlar

### Codec vs. Container (Kapsayıcı)
- **Container (.mp4, .mov, .mxf):** İçinde video, ses ve metadata barındıran "kutu".
- **Codec (H.264, ProRes, AV1):** Görüntü verisini sıkıştıran ve açan matematiksel yöntem.

### 🎨 Chroma Subsampling (Renk Örnekleme)
İnsan gözü parlaklığa (Luma) renkten (Chroma) daha duyarlıdır. Sıkıştırma bu prensibe dayanır:
- **4:2:0:** Renk verisi %75 oranında atılır. (YouTube, Blu-ray, Telefonlar).
- **4:2:2:** Renk verisi %50 oranında korunur. (Yayıncılık, profesyonel kurgu).
- **4:4:4:** Renk verisi %100 korunur. (VFX, Master arşiv).

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

## 📶 Bitrate ve Dosya Boyutu

**Formül:** `Dosya Boyutu = Bitrate x Süre`

| Çözünürlük | Kare Hızı | H.264 (Mbps) | ProRes 422 (Mbps) |
|-----------|-----------|--------------|-------------------|
| **1080p** | 24/25/30  | 8 - 12       | ~117              |
| **1080p** | 50/60     | 12 - 15      | ~234              |
| **4K (UHD)**| 24/25/30  | 35 - 45      | ~470              |
| **4K (UHD)**| 50/60     | 60 - 80      | ~900              |

### Bitrate Kontrol Modları
- **CBR:** Sabit veri hızı. Canlı yayınlar için idealdir.
- **VBR 1-Pass:** Hızlı ama bazı sahnelerde kalite kaybı olabilir.
- **VBR 2-Pass:** İlk geçişte analiz eder, ikinci geçişte verimli dağıtır. En iyi sonuç.

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

## 🎯 Platform Bazlı Tavsiyeler

1.  **YouTube:** H.264 yerine mümkünse **H.265 (HEVC)** kullanın. Daha küçük boyutta daha fazla detay (özellikle 4K'da) sağlar.
2.  **Instagram:** Bitrate'i 15 Mbps'in üstünde tutmayın; Instagram'ın kendi algoritması aşırı yüksek dosyaları bozarak sıkıştırabilir.
3.  **WhatsApp/Telegram:** Göndermeden önce çözünürlüğü 720p'ye düşürmek, izleyici deneyimini hızlandırır.

---

[🏠 README'ye Dön](../README.md)
