# 🎧 Ses ve Ses Tasarımı

> _"Kötü görüntü izlenir ama kötü ses dinlenmez."_ — Birçok film yapımcısı bu konuda hemfikirdir: ses, sinema deneyiminin %50'sinden fazlasıdır.

---

## 🏛️ Ses Katmanları (Audio Layers)

Profesyonel bir ses miksajı şu katmanlardan oluşur:

| Katman | Açıklama | Hedef Seviye (Peak) |
|--------|-----------|-------------|
| **Diyalog** | Konuşmalar, seslendirme | -12 dB ile -6 dB arası |
| **SFX** | Aksiyon destekli ses efektleri | Sahneye göre değişir |
| **Ambiyans** | Mekan arka plan sesi | -30 dB ile -20 dB |
| **Müzik** | Duygu altyapısı | -24 dB ile -12 dB |

### 🧭 Panning (Pan Ayarları)
Seslerin stereo sahnesinde nereye yerleşeceği, gerçekçilik için kritiktir:
- **Diyalog:** Her zaman merkez (Center).
- **Ambiyans:** Geniş stereo (L/R - %100).
- **SFX:** Görüntüdeki nesnenin konumuna göre yerleştirin.

---

## 🎙️ Diyalog İşleme (Dialogue Processing)

### Profesyonel Sinyal Zinciri
```
Noise Reduction → Subtractive EQ → Compressor → Additive EQ → De-Esser → Limiter
```

### 🎚️ EQ Stratejileri
1. **Subtractive EQ (Temizlik):** İstenmeyen frekansları çıkarın. 
   - **High Pass (Low Cut):** 80-100 Hz altını tamamen kesin (Rumble temizliği).
   - **Boxy Sound:** 300-500 Hz arasındaki "kutu" sesini hafifçe düşürün.
2. **Additive EQ (Parlatma):** Sesi güzelleştirin.
   - **Anlaşılırlık:** 3-5 kHz arasını hafifçe artırın.
   - **Hava (Air):** 10-12 kHz üstünü bir "High Shelf" ile parlatın.

### 📉 Sidechain Compression (Ducking)
Müzik ve diyalog aynı frekanslarda çakıştığında kullanılır.
- **Nasıl çalışır?** Diyalog kanalından gelen sinyal, müzik kanalındaki kompresörü tetikler. Diyalog başladığında müzik otomatik olarak (örn: 3-6 dB) kısılır.
- **Parametreler:** Attack (hızlı), Release (orta/yavaş) olmalıdır ki geçiş yumuşak olsun.

---

## 📊 LUFS Standartları (Loudness Units Full Scale)

Modern platformlarda sadece Peak değil, **Loudness** değerleri önemlidir.

| Platform | Hedef (Integral LUFS) | Maks Peak (True Peak) |
|----------|-----------|-----------|
| **YouTube** | -14 LUFS | -1.0 dB |
| **Spotify** | -14 LUFS | -1.0 dB |
| **Netflix** | -27 LUFS | -2.0 dB |
| **TV (EBU R128)** | -23 LUFS | -1.0 dB |

---

## 🔍 Spektral Düzenleme (Spectral Editing)

Geleneksel EQ ile çözülemeyen sorunlar (kuş sesi, telefon zili, siren vb.) için kullanılır.
- **Görsel Düzenleme:** Ses dalgası yerine frekans spektrumuna bakılır.
- **Araçlar:** **iZotope RX**, **Adobe Audition**, **DaVinci Fairlight**.
- **Kullanım:** Sadece istenmeyen sesin bulunduğu frekans ve zaman aralığı "boyanarak" veya "silinerek" temizlenir, geri kalan ses bozulmaz.

---

## 🌊 Ses Efektleri (SFX)

### Foley vs. SFX
- **Foley:** Görüntüye senkronize olarak stüdyoda kaydedilen fiziksel sesler (adım sesi, kıyafet hışırtısı).
- **SFX:** Kütüphanelerden alınan hazır sesler (silah sesleri, araba motoru).

> 💡 **Altın Kural:** "Worldizing" tekniğini kullanın. Stüdyoda kaydedilen kuru bir sesi, sahnedeki odanın akustiğine uydurmak için Reverb (Yankı) ekleyin.

---

## 🛖 Room Tone (Mekan Tonu)

Her çekim ortamının kendine özgü bir "sessizliği" vardır.
- **Neden önemli?** Diyalog klipleri arasındaki mutlak sessizlik izleyiciyi rahatsız eder. Master kanala düşük sesli bir room tone eklemek sürekliliği sağlar.
- **Kayıt Belgelem:** Sette mutlaka en az 1 dakika "herkes sussun" diyerek kayıt alın.

---

[🏠 README'ye Dön](../README.md)
