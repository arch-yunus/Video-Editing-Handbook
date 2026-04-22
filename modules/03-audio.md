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

## 📊 Önemli Frekans Aralıkları

Ses düzenlerken (EQ) hangi aralığın neye karşılık geldiğini bilmek kritiktir:

| Frekans Aralığı | Tanım | Etkisi |
|-----------------|-------|--------|
| **20Hz - 60Hz** | Sub-Bass | Hissedilen ama zor duyulan derinlik. Fazlası "çamurlu" ses yapar. |
| **80Hz - 250Hz** | Low-End | Sesin gövdesi. Erkek sesinin temel frekansları buradadır. |
| **2kHz - 5kHz** | Presence | Netlik ve anlaşılırlık. İnsan kulağının en hassas olduğu yer. |
| **7kHz - 12kHz** | Sibilance | "S", "Ş", "Ç" sesleri. Fazlası kulağı tırmalar (De-esser ile düzeltilir). |
| **15kHz+** | Air | Sesin "havası" ve ferahlığı. |

---

## 🎚️ Dinamik İşleme (Dynamic Processing)

Dinamik aralık, bir sesteki en sessiz ve en yüksek nokta arasındaki farktır.

### 1. Kompresör (Compressor)
Yüksek sesleri kısar, alçak sesleri yükseltir. Sesi "yoğunlaştırır".
- **Threshold:** Kompresörün ne zaman devreye gireceği.
- **Ratio:** Sıkıştırma oranı (Diyalog için genelde 3:1 veya 4:1).
- **Make-up Gain:** Sıkıştırma sonrası kaybedilen genel ses seviyesini geri kazanma.

### 2. Side-chaining (Ducking)
Konuşma başladığında müziğin otomatik olarak kısılması tekniğidir.
- Müziğe bir kompresör atılır ve "Sidechain Input" olarak vokal kanalı seçilir.
- Vokal sinyal gönderdiğinde müzik baskılanır, vokal sustuğunda müzik eski seviyesine döner.

---

## 🔊 Ses Seviye Standartları (Loudness)

Profesyonel dünyada artık "Peak" seviyesi yerine **LUFS** (Loudness Units relative to Full Scale) birimi kullanılmaktadır.

| Platform | Hedef Seviye (Loudness) | Önemli Not |
|----------|------------------------|------------|
| **YouTube / Spotify** | -14 LUFS | Daha yüksek sesler platform tarafından otomatik kısılır. |
| **TV (EBU R128)** | -23 LUFS | Yayıncılık standardı. Dinamik aralık daha fazladır. |
| **Sinema** | -27 LUFS / 82dB SPL | Çok geniş dinamik aralık ve derin sessizlikler. |

> **💡 İpucu:** Miksaj yaparken en yüksek noktanın (True Peak) **-1.0 dB**'i geçmediğinden emin olun.

---

## 🛠️ Profesyonel Ses Katmanları (Audio STEMS)

Kurguda sesleri şu kategorilere ayırarak çalışmak ("checkerboarding") hız kazandırır:
1.  **DX (Dialogue):** Ana diyaloglar ve dış sesler.
2.  **SFX (Sound Effects):** Kapı gıcırtısı, patlama, rüzgar vb.
3.  **Foley:** Karakterlerin ayak sesleri, kıyafet hışırtıları (stüdyoda kaydedilenler).
4.  **BG/Ambiance:** Odanın veya mekanın genel atmosfer sesi.
5.  **MX (Music):** Fon müzikleri ve müzik efektleri.

---

## 🧼 Ses Temizleme (Noise Reduction)
- **Gate:** Belirli bir seviyenin altındaki sesleri (dip gürültüsü) tamamen kapatır.
- **Spectral Repair:** AI araçları (izotope RX vb.) ile ses dalgası üzerindeki istenmeyen bir tıkırtıyı görsel olarak silme.
- **Voice Isolation:** Arka plandaki trafik veya klima sesini diyalogdan ayırma.
- **SFX:** Kütüphanelerden alınan hazır sesler (silah sesleri, araba motoru).

> 💡 **Altın Kural:** "Worldizing" tekniğini kullanın. Stüdyoda kaydedilen kuru bir sesi, sahnedeki odanın akustiğine uydurmak için Reverb (Yankı) ekleyin.

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

### 🔊 Ses Miksaj Zinciri (Mastering Chain)

Profesyonel bir ses elde etmek için şu sıra takip edilmelidir:
1.  **Gürültü Giderici (Denoiser):** AI tabanlı (Voice Isolation) veya parametrik araçlarla arka plan sesini temizleme.
2.  **Parametrik EQ:** Gereksiz frekansları kesme (Low-cut) ve netliği artırma.
3.  **Kompresör (Compressor):** Ses seviyesini dengede tutma (Dinamik aralığı daraltma).
4.  **Limiter:** Sesin belirlenen eşiği (genelde -1 dB veya -3 dB) geçip patlamasını (clipping) önleme.

---

## 👂 Room Tone ve Foley

Ses kurgusunun en az görüntü kurgusu kadar detaylı olması gerekir.
- **Room Tone:** Mekanın sessizliğinin sesi. Diyaloglardaki boşlukları doldurmak için mutlaka her çekimde 30 saniye kaydedilir.
- **Foley:** Görüntüye sonradan eklenen fiziksel ses efektleri (ayak sesi, kıyafet hışırtısı, kapı gıcırtısı). Bu, sahneye derinlik ve gerçekçilik katar.
- **Soundscape (Ambiyans):** Mekanın ruhunu yansıtan trafik, kuş sesleri gibi katmanlar.

---

## 📊 Loudness Standartları (LUFS)

Video çıkışı almadan önce sesin "Loudness" değerini kontrol etmek hayati önem taşır.
| Platform | Hedef LUFS (Loudness Unit Full Scale) |
| :--- | :--- |
| **YouTube / Spotify** | -14 LUFS |
| **Netflix / Disney+** | -27 LUFS (±2 dB) |
| **TV Broadcast (EBU R128)** | -23 LUFS |

> **İpucu:** Eğer sesiniz -14 LUFS'tan daha yüksekse, platformlar sesinizi otomatik olarak kısacaktır. Bu da ses kalitenizin bozulmasına neden olur.
