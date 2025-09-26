# Akbank Derin Öğrenme Bootcamp

🛑Traffic Sign Recognition: Derin Öğrenme ile Trafik İşareti Sınıflandırma
🔹 Giriş

Bu proje, görüntü tabanlı çok sınıflı sınıflandırma problemini çözmeye odaklanmıştır. Proje kapsamında Convolutional Neural Network (CNN) tabanlı bir derin öğrenme modeli geliştirilmiş ve trafik işaretlerinin sınıflandırılması hedeflenmiştir.

Veri seti: Traffic Signs Preprocessed Dataset (Kaggle)
   * Bu veri seti, 43 farklı trafik işareti sınıfına ait 30.000'den fazla ön işlenmiş görüntü içermektedir.

Amaç: Trafik işaretlerini doğru şekilde sınıflandırarak sürücüsüz araçlar, trafik analizi ve akıllı ulaşım sistemlerinde kullanılabilecek bir temel model geliştirmek. 

🔹 Kullanılan Yöntemler ve Model

- **Model Türü:** Convolutional Neural Network (CNN)

- **Kütüphaneler:** TensorFlow & Keras

- **Model Mimarisi (özet):**

  * Birden fazla Conv2D + ReLU katmanları

  * MaxPooling2D katmanları

  * Dropout: Overfitting’i azaltmak için

  * Dense (tam bağlı) katmanlar ve softmax çıkış

- **Optimizasyon:** Adam Optimizer

- **Loss Fonksiyonu:** Categorical Crossentropy

- **Veri Artırma (Data Augmentation):** Modelin genelleme yeteneğini artırmak için

- **Erken Durdurma (Early Stopping):** Overfitting'i önlemek için

🔹 Sonuçlar ve Metrikler

- **Test Kaybı:** 0.3249

- **Test Doğruluğu:** 0.9218

📊 Sınıflandırma Raporu (Özet):

- Ortalama Doğruluk (accuracy): %92

- Makro Ortalama (macro avg F1-score): %86

- Ağırlıklı Ortalama (weighted avg F1-score): %92

➡️ Model özellikle bazı sınıflarda %99 doğruluk göstermiştir (ör. sınıf 10, 13, 15, 16). Bu, modelin belirgin ve görsel açıdan ayırt edici işaretlerde çok iyi genelleme yaptığını gösteriyor. Ancak düşük destekli veya birbirine benzeyen işaretlerde (ör. sınıf 19, 21, 27, 39) performans daha düşüktür -> precision/recall değerleri 0.3–0.6 seviyelerine kadar düşüyor. Bu da modelin sınıflar arası benzerlik ve dengesiz veri sorunları yaşadığını gösteriyor.
Gerçekleştirilen eğitim ve test aşamaları sonucunda, CNN modeli test veri seti üzerinde oldukça başarılı bir performans sergilemiştir.

🔹 Gelecek Çalışmalar

Bu proje ileride şu şekilde geliştirilebilir:
 - Transfer learning (ResNet / EfficientNet / VGG) ile yeniden deneme

 - Veri artırma, sınıf ağırlıkları veya SMOTE benzeri yöntemler ile dengesizlik sorununa müdahale

 - Streamlit/Flask ile küçük bir demo arayüzü (gerçek zamanlı kamera tahmini)

 - Modeli TensorFlow Lite ile mobil cihazlara aktarma

🔹 Linkler
- **Dataset:** https://www.kaggle.com/datasets/valentynsichkar/traffic-signs-preprocessed/data
- **Notebook Çalışmam:** https://www.kaggle.com/code/buseozmntse/cnn-ile-trafik-aretleri-s-n-flama


