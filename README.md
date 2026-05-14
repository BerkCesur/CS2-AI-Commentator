# CS2 AI Video Commentator

**Öğrenci:** Berk Burhan Cesur — 230212023  
**Üniversite:** Ostim Teknik Üniversitesi  
**Ders:** Derin Öğrenme  
**Öğretim Üyesi:** Dr. Murat Şimşek  

---

## Proje Özeti

CS2 highlight kliplerinden otomatik Türkçe açıklama üreten hibrit bir yapay zeka sistemi. 34 adet Faceit/Allstar.gg CS2 highlight klibi üzerinde InternVL2-8B görsel-dil modeli ve YOLO nesne tespiti modeli birlikte kullanılmıştır.

## Demo

![Gradio Demo](gradio_demo.png)

## Kullanılan Teknolojiler

- **InternVL2-8B** — Vision-Language Model (görsel anlama + açıklama üretimi)
- **YOLOv10s CS2** — Nesne Tespiti (CT/T oyuncu tespiti, highlight frame seçimi)
- **Google Translate API** — Türkçe Çeviri
- **Gradio** — Demo Arayüzü
- **FFmpeg** — Video ön işleme

## Sonuçlar

| Metrik | Skor |
|--------|------|
| ROUGE-1 | 0.298 |
| ROUGE-2 | 0.053 |
| ROUGE-L | 0.207 |

## Pipeline

1. FFmpeg ile son 10 saniye kesme (highlight ekranını kaldır)
2. YOLO + hareket skoru ile aksiyon yoğun frame seçimi
3. InternVL2-8B ile harita tespiti (Mirage, Nuke, Anubis...)
4. Few-shot prompting ile İngilizce açıklama üretimi
5. Google Translate ile Türkçeye çeviri

## Dosyalar

| Dosya | Açıklama |
|-------|----------|
| `CS2_AI_Commentator_Final.ipynb` | Proje notebook'u |
| `DEEP_LEARNING_BERK_BURHAN_CESUR_CS2.pdf` | Proje raporu |

## Veri Seti

34 adet CS2 highlight klibi — Faceit / Allstar.gg platformları  
Google Drive: `/CS2_Video_Caption/CS-2_Videolar/`  
Video boyutu nedeniyle GitHub'a yüklenmemiştir.
