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
