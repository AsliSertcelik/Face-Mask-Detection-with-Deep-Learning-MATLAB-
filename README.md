
# Derin Öğrenme ile Yüz Maskesi Tespiti (MATLAB)

## Proje Açıklaması

Bu proje, derin öğrenme teknikleri kullanılarak bir kişinin yüz maskesi takıp takmadığını tespit etmeyi amaçlamaktadır. Çalışmada transfer öğrenme yaklaşımı kullanılarak önceden eğitilmiş evrişimli sinir ağı (CNN) modellerinden faydalanılmıştır.

Model geliştirme süreci MATLAB Deep Learning Toolbox kullanılarak gerçekleştirilmiştir.

Veri seti kaggle üzerinden indirilebilir.
https://www.kaggle.com/datasets/omkargurav/face-mask-dataset

---

##  Veri Seti

Bu projede Kaggle platformundan elde edilen **Face Mask Dataset** kullanılmıştır.

* Sınıflar:

  * with_mask (maskeli)
  * without_mask (masksız)

* Kullanılan toplam görüntü sayısı: =7553
* with mask=3725
* without mask=3825

* Veri bölünmesi:

  * Eğitim: %80
  * Doğrulama: %10
  * Test: %10

---

## Model Mimarisi

Başlangıçta DenseNet mimarisi değerlendirilmiş, ancak yüksek hesaplama maliyeti ve uzun eğitim süresi nedeniyle tercih edilmemiştir.

✔ Kullanılan model: **MobileNetV2**
✔ Yaklaşım: **Transfer Learning (Transfer Öğrenme)**

Yapılan değişiklikler:

* Son tam bağlantılı katman değiştirilmiştir
* Çıkış katmanı ikili sınıflandırmaya uygun hale getirilmiştir

---

##  Eğitim Detayları

* Optimizasyon algoritması: Adam
* Öğrenme oranı: 0.001
* Epoch sayısı: 5
* Mini-batch boyutu: 16

### Veri Artırma (Data Augmentation)

* Döndürme (rotation)
* Kaydırma (translation)
* Ölçekleme (scaling)

---

##  Sonuçlar

| Metrik              | Değer  |
| ------------------- | ------ |
| Doğruluk (Accuracy) | %99.21 |
| Precision           | %98.93 |
| Recall              | %99.46 |
| F1-Score            | %99.20 |
| Specificity         | %98.96 |

---

##  Değerlendirme

### Confusion Matrix

Model, sınıflandırma görevinde oldukça yüksek başarı göstermiş ve çok düşük hata oranı ile çalışmıştır.

### ROC Eğrisi

ROC eğrisi incelendiğinde modelin sınıfları başarıyla ayırt edebildiği ve yüksek AUC değerine sahip olduğu görülmektedir.

---

##  Sonuç

MobileNetV2 tabanlı model, düşük hesaplama maliyetine rağmen yüksek doğruluk oranı elde etmiştir. DenseNet modeline kıyasla daha hızlı eğitim süresi sunması önemli bir avantaj sağlamıştır.

Bu model, gerçek zamanlı uygulamalarda kullanılabilecek potansiyele sahiptir.

---

## 🛠️ Kullanılan Teknolojiler

* MATLAB
* Deep Learning Toolbox
* Computer Vision Toolbox

---

##  Gelecek Çalışmalar

* Daha büyük veri setleri ile test edilmesi
* Gerçek zamanlı sistemlere entegrasyon
* Farklı model mimarileri ile karşılaştırma

Aslı Sertçelik

English Below

# Face-Mask-Detection-with-Deep-Learning-MATLAB-
This project aims to detect whether a person is wearing a face mask using deep learning techniques. A transfer learning approach was applied using pre-trained convolutional neural networks.  The model was trained and evaluated using MATLAB Deep Learning Toolbox.
# Face Mask Detection with Deep Learning (MATLAB)

##  Project Overview

This project aims to detect whether a person is wearing a face mask using deep learning techniques. A transfer learning approach was applied using pre-trained convolutional neural networks.

The model was trained and evaluated using MATLAB Deep Learning Toolbox.

The dataset can be downloeded from kaggle.
https://www.kaggle.com/datasets/omkargurav/face-mask-dataset

---
---

## Dataset

The dataset used in this project is the **Face Mask Dataset** obtained from Kaggle.

* Classes:

  * with_mask
  * without_mask

* Total images used: =7553
* with mask =3725
* without mask=3828

* Train / Validation / Test split:

  * Training: 80%
  * Validation: 10%
  * Test: 10%

---

##  Model Architecture

Initially, the DenseNet architecture was considered. However, due to its high computational cost and long training time, it was replaced with a more efficient model.

✔ Final Model: **MobileNetV2**
✔ Approach: **Transfer Learning**

Modifications:

* Final fully connected layer replaced
* Output adapted for binary classification

---

## Training Details

* Optimizer: Adam
* Learning Rate: 0.001
* Epochs: 5
* Mini-batch size: 16
* Data Augmentation:

  * Rotation
  * Translation
  * Scaling

---

##  Results

| Metric      | Value  |
| ----------- | ------ |
| Accuracy    | 99.21% |
| Precision   | 98.93% |
| Recall      | 99.46% |
| F1-Score    | 99.20% |
| Specificity | 98.96% |

---

##  Evaluation

### Confusion Matrix

The model achieved very high classification performance with minimal misclassification.

### ROC Curve

The ROC curve demonstrates strong separability between classes with high AUC.

---

## Conclusion

The MobileNetV2-based model achieved high accuracy while maintaining low computational cost. Compared to DenseNet, it provides a more efficient solution, especially for systems with limited hardware resources.

---

##  Technologies Used

* MATLAB
* Deep Learning Toolbox
* Computer Vision Toolbox

---

## Future Work

* Test on larger datasets
* Real-time deployment
* Comparison with other deep learning architectures

---

Aslı Sertçelik

