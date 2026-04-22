# ⚙️ Post-Prodüksiyon İş Akışı

> Profesyonel bir kurgu süreci, karman çorman bir zaman çizelgesinden (timeline) kaçınmak için sistematik aşamalardan oluşur. Her aşama bir sonrakinin temelini oluşturur.

---

## 📁 1. Organizasyon (Media Management)

İyi bir kurgu, iyi bir organizasyonla başlar. **"Organize olmak zaman kaybettirir" değil, "organize olmamak daha fazla zaman kaybettirir."**

### Önerilen Klasör Hiyerarşisi

```
Proje_Adı/
├── 01_RAW_FOOTAGE/       # Ham kamera görüntüleri (asla silme!)
│   ├── Camera_A/
│   └── Camera_B/
├── 02_AUDIO/             # Harici ses kayıtları, müzikler
│   ├── Dialogue/
│   ├── SFX/
│   └── Music/
├── 03_GRAPHICS/          # Logolar, motion graphics, alt yazılar
├── 04_EXPORTS/           # Çıktı dosyaları (farklı formatlarda)
│   ├── Review_Cuts/
│   └── Final/
└── 05_PROJECT_FILES/     # .prproj, .drp, .fcpx dosyaları
```

### Kural: 3-2-1 Yedekleme
- **3** kopya bulundur.
- **2** farklı medyada (örn: HDD + SSD).
- **1** tanesini farklı fiziksel konumda (bulut veya offsite).

### 🏷️ Metadata ve İsimlendirme Metodolojisi
Sadece klasörleri değil, dosyaları da akıllıca isimlendirin:
- `YYYYMMDD_Sahne_Plan_Take` (Örn: `20231024_S01_P02_T01.mov`).
- **Tagging:** Kurgu yazılımı içinde (Premiere Metadata veya Resolve Metadata) çekimlere "Good Take", "Must Use" gibi etiketler ekleyerek arama sürecini hızlandırın.

---

## 🖥️ 2. Proxy Oluşturma (Proxy Workflow)

4K/6K/8K çekimler düzenleme yaparken sistemi yavaşlatır. **Proxy**, ham görüntünün düşük çözünürlüklü kopyasıdır.

| Format      | Proxy Çözünürlüğü | Önerilen Codec |
|-------------|-------------------|----------------|
| 4K (3840x2160) | 1920x1080 veya 1280x720 | ProRes Proxy / DNxHD LB |
| 6K / 8K     | 2048x1080 veya daha düşük | ProRes 422 LT |

> **💡 İpucu:** DaVinci Resolve, Premiere Pro ve Final Cut Pro proxy iş akışlarını otomatik yönetebilir. Export aşamasında orijinal kaliteli dosyaya geri döner.

### 🌐 Offline vs. Online Editing
- **Offline Editing:** Düşük çözünürlüklü (Proxy) dosyalarla hikayeyi kurma aşaması. Sistem performansını maksimize eder.
- **Online Editing:** Picture Lock sonrası orijinal yüksek çözünürlüklü dosyalara (RAW/Log) geri dönüp renk ve efektlerin uygulandığı aşama.

---

## 🔗 3. Senkronizasyon (Syncing)

Harici ses kaydediciler (Zoom H6, Sound Devices gibi) kullanıldığında ses ve görüntünün eşleştirilmesi gerekir.

**Yöntemler:**
1. **Klap tahtası (Slate):** Fiziksel klap sesi ve görüntüsüyle elle sync alma.
2. **Waveform Matching:** Yazılımın ses dalgalarını karşılaştırarak otomatik eşleştirmesi (Premiere, Resolve, Plural Eyes).
3. **Timecode:** Profesyonel setlerde kamera ve ses cihazlarını aynı timecode'a bağlama.

---

## ✂️ 4. Kaba Kurgu (Rough Cut / Assembly Cut)

Hikayenin ham iskeleti oluşturulur. Bu aşamada mükemmellik aranmaz.

- Kullanılabilir çekimler seçilir ("selects" veya "hero clips").
- Gereksiz boşluklar, hatalı çekimler ve kötü kareler çıkarılır.
- Kabul edilebilir uzunluk, final çıktının ~2-3 katı olabilir.

---

## 🎯 5. İnce Kurgu (Fine Cut)

Ritim, nefes ve tempo bu aşamada şekillenir.

- **Pacing:** Sahnenin hızı duygusal tonla uyumlu hale getirilir.
- **Geçişler:** Ani geçişler (hard cut) veya daha yumuşak geçişler (dissolve, dip to black) eklenir.
- **Alt Yazı ve Grafikler:** Lower thirds, title kartları eklenir.

---

## 🔒 6. Kilit (Picture Lock)

**En kritik aşamalardan biri.** Görüntü kurgusunun tamamlanıp onaylandığı nokta.

> ⚠️ **Uyarı:** Picture Lock sonrası herhangi bir kesme yapılırsa ses tasarımı ve renk çalışması sıfırdan başlamak zorunda kalabilir. Bu süreci müşteri/yönetmen onayıyla belgele.

---

## 🔄 6.5. Round-Tripping (Yazılımlar Arası Geçiş)
Profesyonel projelerde kurgu Premiere'de yapılıp renk için Resolve'a gönderilebilir.

**İş Akışı:**
1. **Premiere'den Export:** Timeline'ı basitleştirin (sadece video trackleri kalsın), `XML` veya `AAF` olarak export edin.
2. **Resolve'a Import:** XML dosyasını import ederek orijinal medya dosyalarına linkleyin (Conforming).
3. **Color Grading:** Renk işlemleri tamamlanır.
4. **Geri Dönüş:** Render alıp (yine XML ile) Premiere'e geri dönün veya final render'ı Resolve'dan yapın.

---

## 🎧 7. Ses Tasarımı ve Miksaj

Detaylar için → **[03-audio.md](./03-audio.md)**

---

## 🎨 8. Renk (Color Pipeline)

Detaylar için → **[04-color.md](./04-color.md)**

---

## 📤 9. Dışa Aktarma (Delivery)

Detaylar için → **[06-export.md](./06-export.md)**

---

[🏠 README'ye Dön](../README.md)
