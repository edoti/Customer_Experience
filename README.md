# 🎯 Customer Experience Project – Interactions per Minute Prediction

## 📌 Proje Amacı

Bu proje kapsamında, müşterilerin siteyi ziyaret ettiklerinde **dakika başına kaç etkileşimde** bulunduklarını tahmin etmek hedeflenmiştir.  
Bu amaçla iki farklı regresyon modeli (Random Forest ve Decision Tree) kullanılarak model performansları karşılaştırılmıştır.

---

## 🔍 Kullanılan Veri Seti

- **Kaynak:** [Kaggle - Customer Experience Dataset](https://www.kaggle.com/datasets/ziya07/customer-experience-dataset)
- **Gözlem Sayısı:** 1000
- **Özellikler:** Yaş, cinsiyet, görüntülenen ürün sayısı, memnuniyet skoru, geri bildirim, zaman, etkileşim sayısı vb.
- **Türetilmiş Hedef Değişken:**  
  `Interactions_per_Minute = Num_Interactions / Time_Spent_on_Site`

---

## 🧠 Modelleme Süreci

### ✨ Hedef Değişken
- `Interactions_per_Minute` (dakika başına işlem sayısı)

### 🔨 Kullanılan Modeller
- `RandomForestRegressor`
- `DecisionTreeRegressor`

### 📊 Veri Ön İşleme
- Eksik değer: Yok
- Aykırı değer: Yok
- Kategorik değişkenler: One-Hot Encoding (veya zaten encode edilmiş)

---

## 📈 Model Karşılaştırması

| Model               | RMSE (Hata) | MAE (Ortalama Hata) | R² Score (Açıklayıcılık) |
|---------------------|-------------|----------------------|---------------------------|
| **Random Forest**   | ✅ **0.0423** | ✅ **0.0159**         | ✅ **0.9863**              |
| **Decision Tree**   | ❗ 0.0484    | ❗ 0.0262              | ❗ 0.9821                   |

---

## 📌 Yorumlar ve Sonuç

- **Random Forest**, daha düşük hata oranı ve daha yüksek açıklayıcılık oranı ile bu tahminleme görevi için daha başarılı olmuştur.
- Özellikle `Time_Spent_on_Site` ve `Num_Interactions` gibi temel değişkenler modelin tahmin başarısında belirleyici olmuştur.
- **Decision Tree** ise daha sade bir yapıya sahip olsa da genelleme gücü Random Forest'a göre zayıftır.

---


## ✅ Kullanılan Kütüphaneler

- pandas, numpy
- matplotlib, seaborn
- scikit-learn

---

## ✍️ Hazırlayan

Eda Korkmaz  
2025  

