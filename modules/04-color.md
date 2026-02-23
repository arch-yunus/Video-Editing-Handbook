# 🎨 Renk Düzenleme (Color Pipeline)

> Renk, bir filmin kimliğidir. Aynı sahne farklı renk işlemleriyle tamamen farklı duygular yaratabilir.

---

## 🔑 İki Temel Kavram

### Color Correction (Renk Doğrulama)
**Teknik** bir süreçtir. Görüntünün "doğal" ve teknik olarak doğru görünmesini sağlamak hedeflenir.

- Beyaz ayarı (White Balance) düzeltme
- Pozlama (Exposure) ve parlaklık dengeleme
- Kontrastın doğal aralığa çekilmesi
- Farklı kameralardan gelen görüntüleri birbirine eşitleme (matching)

### Color Grading (Renk Derecelendirme)
**Sanatsal** bir süreçtir. Videoya bilinçli bir stil, atmosfer ve duygu katmak hedeflenir.

| Film | Renk Stili |
|------|-----------|
| *The Matrix* | Yeşil-sarı tonlar (dijital dünya hissi) |
| *Mad Max: Fury Road* | Turuncu ve mavi kontrast |
| *La La Land* | Canlı, sature pastel tonlar |
| *Se7en* | Soğuk, desature, grimsi |

---

## 📊 Renk Araçları (Scopes)

Gözünüze güvenmeyin — **Scopes** kullanın. Monitörünüzün rengi yanlış kalibre edilmiş olabilir.

| Scope | Görevi |
|-------|--------|
| **Waveform** | Parlaklık seviyelerini (luma) gösterir |
| **Parade** | R, G, B kanallarını ayrı ayrı inceleme |
| **Vectorscope** | Renk tonu (hue) ve doygunluk (saturation) |
| **Histogram** | Tüm tonal değerlerin dağılımı |

---

## 🖐️ Primary Color Wheels

Her renk grading yazılımı şu üç temel çarkı sunar:

```
[Shadows / Siyahlar]   [Midtones / Orta Tonlar]   [Highlights / Parlaklar]
```

- **Shadows:** Karanlık alanların rengi ve seviyesi
- **Midtones:** Orta gri alanlar (en çok cilt tonunu etkiler)
- **Highlights:** En parlak alanlar (gökyüzü, lambalar)

---

## 🎛️ LUT (Look-Up Table)

Önceden hazırlanmış renk dönüşüm tablolarıdır.

### LUT Türleri

| Tür | Amaç |
|-----|------|
| **Technical LUT** | Log formatı → Rec.709 dönüşümü (kamera üreticisi sağlar) |
| **Creative LUT** | Sanatsal stil uygulamak |

### Doğru LUT Kullanım Sırası
```
1. Ham Görüntü (Log: S-Log3, V-Log, C-Log)
2. Technical LUT (Log → Rec.709)
3. Color Correction (beyaz ayarı, pozlama düzeltme)
4. Creative LUT veya manuel grade
5. Output LUT (Rec.709 → DCI-P3 veya HDR)
```

> ⚠️ **Hata:** Üstüne üstlük Creative LUT uygulamak. LUT'lar doğru başlangıç noktasından sonra anlam taşır.

---

## 🌈 Renk Teorisi: Complementary Colors

**Orange & Teal** komb neden bu kadar popüler?

İnsan cilt tonu turuncu tayfın içindedir. Karşıt renk (complementary) ise mavi-yeşil (teal). Bu kontrast:
- Cilt tonunu ön plana çıkarır
- Sinematik bir derinlik yaratır
- Gözü hoş bir gerilim sağlar

---

## 🛠️ Popüler Renk Araçları

| Yazılım | Platform | Maliyet |
|---------|----------|---------|
| **DaVinci Resolve** | Windows/Mac/Linux | Ücretsiz (Studio versiyonu ücretli) |
| **Adobe Premiere Pro** | Windows/Mac | Abonelik |
| **Final Cut Pro** | Mac | Tek seferlik ücret |
| **Filmora** | Windows/Mac | Abonelik / Ücretsiz |

---

[🏠 README'ye Dön](../README.md)
