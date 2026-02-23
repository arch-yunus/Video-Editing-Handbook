# 🎧 Ses ve Ses Tasarımı

> _"Kötü görüntü izlenir ama kötü ses dinlenmez."_ — Birçok film yapımcısı bu konuda hemfikirdir: ses, sinema deneyiminin %50'sinden fazlasıdır.

---

## 🏛️ Ses Katmanları (Audio Layers)

Profesyonel bir ses miksajı şu katmanlardan oluşur:

| Katman | Açıklama | Hedef Seviye |
|--------|-----------|-------------|
| **Diyalog** | Konuşmalar, seslendirme | -12 dB ile -6 dB arası |
| **SFX** | Aksiyon destekli ses efektleri | Sahneye göre değişir |
| **Ambiyans** | Mekan arka plan sesi | -30 dB ile -20 dB |
| **Müzik** | Duygu altyapısı | -18 dB ile -12 dB (diyaloğun altında) |

---

## 🎙️ Diyalog İşleme (Dialogue Processing)

### Temel Zincir
```
Ham Ses → Noise Reduction → EQ → Compression → De-Esser → Maximizer
```

### Adım Adım

**1. Noise Reduction (Gürültü Azaltma)**
- Klip başındaki "sessiz" kısımdan gürültü profili al.
- Araçlar: iZotope RX, Premiere Pro'nun Denoise efekti, Audacity.

**2. EQ (Ekolayzer)**
- **80 Hz altını kes** (HP Filter): Perde sesi, havalandırma gürültüsü.
- **2-4 kHz'i hafif artır:** Ses anlaşılırlığını artırır.
- **Sibilance (5-8 kHz):** Fazla tiz "s" seslerini kontrol et.

**3. Compression**
- Ses dinamiklerini dengeler; alçak sesler yükselir, yüksek sesler baskılanır.
- Önerilen oran: **3:1 ile 6:1** arası başla.

**4. LUFS Hedefi**
| Platform | Hedef LUFS |
|----------|-----------|
| YouTube | -14 LUFS |
| Instagram | -16 LUFS |
| Netflix | -27 LUFS (gece sahneleri) / -15 LUFS (genel) |
| Sinema | -23 LUFS (Dolby) |

---

## 🌊 Ses Efektleri (SFX)

### Foley vs. SFX Kütüphanesi

| Foley | SFX Kütüphanesi |
|-------|----------------|
| Canlı kaydedilen el yapımı sesler | Önceden kaydedilmiş, hazır sesler |
| Ayak sesleri, giysi hışırtısı, vb. | Patlama, araba, doğa sesleri |
| Daha özgün ve karakteristik | Hızlı ve pratik |

### Önerilen Ücretsiz Kaynaklar
- [Freesound.org](https://freesound.org) — Topluluk destekli, CC lisanslı
- [Pixabay Sound](https://pixabay.com/sound-effects) — Telif hakkı yok
- [BBC Sound Effects](https://sound-effects.bbcrewind.co.uk) — 16.000+ ücretsiz efekt

---

## 🎵 Müzik Editörlüğü

### Müziği Kurguya Uydurmak (Musicalize the Cut)

1. **Hit Point'lere kes:** Müziğin vurgu anlarında kesme yap.
2. **Fade In / Fade Out:** Müzik sahneler arasında yumuşakça giriş çıkış yapmalı.
3. **Ducking:** Diyalog başladığında müzik otomatik kısılır. (Adobe Premiere'de "Auto Ducking", DaVinci Resolve'da "Fairlight Ducking" özelliği mevcuttur.)

### Lisans Konuları

| Lisans Türü | Kullanım |
|-------------|----------|
| **Royalty-Free** | Bir kez ödeme, sınırsız kullanım |
| **Creative Commons (CC0)** | Tamamen ücretsiz, attribution gerekebilir |
| **Sync License** | Film/reklam için şarkı hakkı satın alma |
| **Copyrighted (YouTube)** | İçerik ID tetikler, para kaybına neden olabilir |

---

## 🛖 Room Tone (Mekan Tonu)

Her çekim ortamının kendine özgü bir "sessizliği" vardır: klima uğultusu, dışarıdan trafik sesi vb.

**Neden önemli?** Diyalog klipleri arasındaki boşluklar "ölü" ve yapay durur. Room tone bu boşluğu doldurarak sahneyi gerçekçi kılar.

**Nasıl kaydedilir?** Setde kamera gelmeden önce 30-60 saniye sadece ortamın sesini kaydet. Bu ses kurgu masasında "sessiz anları" doldurmak için kullanılır.

---

[🏠 README'ye Dön](../README.md)
