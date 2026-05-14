# CS2-AI-Commentator
CS2 highlight kliplerinden otomatik Türkçe açıklama | InternVL2-8B + YOLO | ROUGE-L: 0.207
# CS2 AI Video Commentator

**Öğrenci:** Berk Burhan Cesur — 230212023  
**Üniversite:** Ostim Teknik Üniversitesi  
**Ders:** Derin Öğrenme  
**Öğretim Üyesi:** Dr. Murat Şimşek  

## Proje Özeti

CS2 highlight kliplerinden otomatik Türkçe açıklama üreten hibrit bir yapay zeka sistemi.
34 adet Faceit/Allstar.gg CS2 highlight klibi üzerinde InternVL2-8B görsel-dil modeli
ve YOLO nesne tespiti modeli birlikte kullanılmıştır.

## Kullanılan Teknolojiler

- InternVL2-8B (Vision-Language Model)
- YOLOv10s CS2 (Nesne Tespiti)
- Google Translate API (Türkçe Çeviri)
- Gradio (Demo Arayüzü)

## Sonuçlar

| Metrik | Skor |
|--------|------|
| ROUGE-1 | 0.298 |
| ROUGE-2 | 0.053 |
| ROUGE-L | 0.207 |

## Pipeline

1. FFmpeg ile son 10 saniye kesme
2. YOLO + hareket skoru ile highlight frame seçimi
3. InternVL2-8B ile harita tespiti
4. Few-shot prompting ile açıklama üretimi
5. Google Translate ile Türkçeye çeviri

## Veri Seti

34 adet CS2 highlight klibi — Faceit / Allstar.gg platformları  
Google Drive: `/CS2_Video_Caption/CS-2_Videolar/`
