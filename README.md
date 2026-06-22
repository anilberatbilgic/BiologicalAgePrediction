# 🧬 Biological Age Prediction

Predicting a person's *biological* age from molecular biomarker data using machine learning regression.

![Python](https://img.shields.io/badge/Python-3.x-blue.svg)
![scikit-learn](https://img.shields.io/badge/scikit--learn-Regression-orange.svg)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626.svg)

**🌐 Language:** English · [Türkçe](#-türkçe)

## ⏳ Overview

Chronological age (the candles on your cake) and **biological age** (how old your body actually behaves) can differ. Molecular markers carry that signal. This project trains a regression model to estimate biological age from biomarker measurements — a building block of aging and longevity research.

## 📊 Dataset

- **`data.csv`** — per-sample biomarker measurements (feature matrix; identifier columns such as sample accessions are dropped before modeling).
- **`Ages.csv`** — the corresponding ages used as the regression target.

## 🧠 Approach

1. **Preprocessing** — merge features with targets, drop identifier columns, check/handle missing values, standardize with `StandardScaler`.
2. **Split** — `train_test_split` into training and test sets.
3. **Model** — train a **Random Forest Regressor**.
4. **Evaluation** — report **MAE** (mean absolute error, in years) and **R²** to measure how closely predictions track true age.

## 🛠️ Tech Stack

`Python` · `pandas` · `numpy` · `scikit-learn` (RandomForestRegressor, StandardScaler, metrics)

## ▶️ How to Run

```bash
pip install pandas numpy scikit-learn matplotlib
jupyter notebook BiologicalAgePrediction.ipynb
```

Place `data.csv` and `Ages.csv` next to the notebook, then run all cells.

---

<a name="-türkçe"></a>
## 🇹🇷 Türkçe

### Genel Bakış
Kronolojik yaş (pastandaki mumlar) ile **biyolojik yaş** (vücudunun gerçekte ne kadar yaşlı davrandığı) farklı olabilir. Moleküler belirteçler bu sinyali taşır. Bu proje, biyobelirteç ölçümlerinden biyolojik yaşı tahmin eden bir regresyon modeli eğitir — yaşlanma ve uzun ömür araştırmalarının bir yapı taşı.

### Veri Seti
- **`data.csv`** — örnek başına biyobelirteç ölçümleri (öznitelik matrisi; örnek erişim numarası gibi kimlik sütunları modellemeden önce atılır).
- **`Ages.csv`** — regresyon hedefi olarak kullanılan karşılık gelen yaşlar.

### Yaklaşım
1. **Ön işleme** — öznitelikler hedeflerle birleştirilir, kimlik sütunları atılır, eksik veri kontrol edilir, `StandardScaler` ile standartlaştırılır.
2. **Bölme** — `train_test_split` ile eğitim/test ayrımı.
3. **Model** — **Random Forest Regressor** eğitilir.
4. **Değerlendirme** — tahminlerin gerçek yaşı ne kadar yakaladığını ölçmek için **MAE** (yıl cinsinden ortalama mutlak hata) ve **R²** raporlanır.

### Teknolojiler
`Python` · `pandas` · `numpy` · `scikit-learn`

### Çalıştırma
```bash
pip install pandas numpy scikit-learn matplotlib
jupyter notebook BiologicalAgePrediction.ipynb
```
`data.csv` ve `Ages.csv` dosyalarını notebook'un yanına koy ve tüm hücreleri çalıştır.
