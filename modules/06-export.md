# 📤 Dışa Aktarma ve Codec'ler

> Codec seçimi içeriğin kalitesini, dosya boyutunu ve platform uyumluluğunu doğrudan etkiler. "En iyi codec" diye bir şey yoktur; **amaca en uygun codec** vardır.

---

## 🔑 Temel Kavramlar

### Codec vs. Container (Kapsayıcı)

```
Container (.mp4, .mov, .mkv) = Zarfın şekli
Codec (H.264, ProRes, H.265) = Zarfın içindeki bilgiyi nasıl paketlediği
```

| Container | İçerebileceği Codec'ler |
|-----------|------------------------|
| `.mp4` | H.264, H.265, AAC |
| `.mov` | ProRes, DNxHD, H.264 |
| `.mkv` | Hemen hemen her şey |
| `.mxf` | XDCAM, AVC-Intra (yayın) |

---

## 📦 Codec Karşılaştırma Tablosu

| Codec | Kullanım Amacı | Dosya Boyutu | Kalite |
|-------|---------------|-------------|--------|
| **H.264** | Web, YouTube, Instagram | Küçük | İyi |
| **H.265 (HEVC)** | 4K web, eşit kalitede %40 küçük boyut | Küçük | Çok İyi |
| **ProRes 422** | Post-prodüksiyon ara format | Büyük | Mükemmel |
| **ProRes 4444** | VFX, alpha kanallı kompoziting | Çok Büyük | Kayıpsıza Yakın |
| **DNxHD / DNxHR** | Avid tabanlı post workflow | Büyük | Mükemmel |
| **AV1** | Yeni nesil web yayını | Küçük | Çok İyi |

---

## 📊 Bitrate (Bit Hızı) Rehberi

Bitrate, videonun saniye başına düşen veri miktarıdır (Mbps veya kbps). Yüksek bitrate = daha az sıkıştırma = daha iyi kalite.

### YouTube Önerilen Bitrate (H.264)

| Çözünürlük | FPS | Önerilen Bitrate |
|-----------|-----|-----------------|
| 1080p | 24/30 | 8 Mbps |
| 1080p | 60 | 12 Mbps |
| 4K | 24/30 | 35-45 Mbps |
| 4K | 60 | 53-68 Mbps |

### Instagram Önerilen Bitrate

| Format | Önerilen |
|--------|----------|
| Reels / Feed | 3.5 Mbps |
| Stories | 10 Mbps (sıkıştırılacak) |

> 💡 **İpucu:** Instagram içeriği her zaman sıkıştırır. Yüklemeden önce **çok yüksek bitrate** kullan; Instagram sıkıştırırken mümkün olan en yüksek kaliteyi korur.

---

## 🖥️ Çözünürlük ve Kare Oranları (Frame Rates)

| Frame Rate | Kullanım Alanı |
|-----------|--------------|
| **23.976 fps** | Sinematik film standartı |
| **25 fps** | PAL (Avrupa TV standardı) |
| **29.97 fps** | NTSC (Amerikan TV standardı) |
| **60 fps** | Oyun, spor, aksiyon çekimi |
| **120+ fps** | Yavaş çekim (Slow Motion) |

---

## 🎯 Platform Bazlı Export Şablonları

### YouTube (H.265 / HEVC, 4K)
```
Codec:     H.265 / HEVC
Container: .mp4
Video Bitrate: 45 Mbps (4K 30fps)
Keyframe:  Each Frame (veya Every 2 seconds)
Audio:     AAC, 48 kHz, 320 kbps
Color Space: Rec.709
```

### Instagram Reels (1080p)
```
Codec:     H.264
Container: .mp4
Video Bitrate: 10-15 Mbps
Boyut:     1080x1920 (dikey) veya 1080x1080 (kare)
Audio:     AAC, 44.1 kHz, 192 kbps
Süre:      Max 90 saniye
```

### Sinema / DCP (Digital Cinema Package)
```
Codec:     JPEG2000
Çözünürlük: 2048x1080 (2K) veya 4096x2160 (4K DCI)
Audio:     PCM 48 kHz / 96 kHz
```

---

## ⚡ Render Hızlandırma İpuçları

- **GPU Hızlandırma:** Premiere, Resolve ve Final Cut NVIDIA/AMD GPU'larını kullanır. Donanım hızlandırmayı (Hardware Encoding) etkinleştir.
- **Proxy Export:** Önce düşük çözünürlüklü bir preview render al (review için). Onay sonrası final kalitede render et.
- **Smart Render:** Eğer proje orijinal medyayla aynı codec'teyse, yalnızca kesimleri yeniden render et.

---

[🏠 README'ye Dön](../README.md)
