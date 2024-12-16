# **FACIAL EXPRESSION DETECTION**

Bu proje, yüz ifadelerini algılamak ve sınıflandırmak için oluşturulmuştur.  
Roboflow kullanılarak hazırlanmış YOLOv7 tabanlı model eğitilmiştir.  
Google Colab ortamında çalıştırılarak tekrar eğitilmiştir.

Bu projede algılanan ifadeler şunlardır:  
- **Mutlu**
- **Üzgün**
- **Kızgın**
- **Nötr**
- **Korku**
- **Tiksinti**

---

## **DATASET**

Datasete ulaşmak için: [DATASET](https://universe.roboflow.com/inside-out-rfapn/inside-out/)

### **Dataset Versiyonları:**
- **v1 (İlk hali):**
  - Toplam görsel sayısı: **234**
  
- **v2 (Geliştirilmiş hali):**
  - Yeni görüntüler eklenmiştir.  
  - Toplam görsel sayısı: **326**
  
- **v3 (Görüntü artırımı uygulanmış hali):**
  - **Uygulanan görüntü artırma yöntemleri:**
    - **Flip:** Horizontal  
    - **Crop:** %5 ile %10 arası  
    - **Bounding Box Rotation:** -15° ile +15° arası  
    - **Bounding Box Brightness:** -10% ile +10% arası  
    - **Bounding Box Blur:** 2px'e kadar  
    - **Bounding Box Noise:** %5’e kadar  

---

## **Model Test Komutları**

- **Görsel yükleyerek test etmek için:**
   ```bash
   python detect.py --weights models/best.pt --source example.jpg

- **Kamera ile eşzamanlı test etmek için:**
   ```bash
   python detect.py --weights models/best.pt --source 0
