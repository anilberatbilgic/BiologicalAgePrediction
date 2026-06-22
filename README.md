# 🧬 Biological Age Prediction

Predicting **biological age from gut-microbiome composition** with a Random Forest regressor.

![Python](https://img.shields.io/badge/Python-3.x-blue.svg)
![scikit-learn](https://img.shields.io/badge/scikit--learn-RandomForestRegressor-orange.svg)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626.svg)

**🌐 Language:** English · [Türkçe](#-türkçe)

## ⏳ Overview

Two people of the same calendar age can be biologically older or younger. This project asks whether the **gut microbiome** carries that signal — estimating a person's age purely from the relative abundances of microbial taxa living in them. It's a small window into the fast-growing field of microbiome & aging research.

## 📊 Dataset

Two files merged on the `Sample Accession` key:

- `data.csv` — **microbiome composition** per sample: relative abundances of microbial taxa (e.g. `k__Archaea|p__Euryarchaeota|...`).
- `Ages.csv` — the **Age** of each sample (the regression target).

## 🧠 Approach

1. **Preprocessing** — merge microbiome features with ages on `Sample Accession`; drop identifier/duplicate columns; check for missing values.
2. **Features / target** — `X` = microbiome abundances, `y` = `Age`.
3. **Scaling** — `StandardScaler`.
4. **Model** — `RandomForestRegressor` with a train/test split.
5. **Evaluation** — **MAE** (mean absolute error, in years) and **R²**.

## 🛠️ Tech Stack

`Python` · `pandas` · `numpy` · `scikit-learn` (RandomForestRegressor, StandardScaler, metrics)

## ▶️ How to Run

```bash
pip install pandas numpy scikit-learn matplotlib
jupyter notebook BiologicalAgePrediction.ipynb
```

Place `data.csv` and `Ages.csv` beside the notebook, then run all cells.

---

<a name="-türkçe"></a>
## 🇹🇷 Türkçe

### Genel Bakış
Aynı takvim yaşındaki iki kişi biyolojik olarak daha yaşlı ya da daha genç olabilir. Bu proje, **bağırsak mikrobiyomunun** bu sinyali taşıyıp taşımadığını sorar — bir kişinin yaşını yalnızca içinde yaşayan mikrobiyal taksonların göreli bolluklarından tahmin eder. Hızla büyüyen mikrobiyom & yaşlanma araştırmalarına küçük bir pencere.

### Veri Seti
`Sample Accession` anahtarıyla birleştirilen iki dosya:

- `data.csv` — örnek başına **mikrobiyom kompozisyonu**: mikrobiyal taksonların göreli bollukları (ör. `k__Archaea|p__Euryarchaeota|...`).
- `Ages.csv` — her örneğin **Yaşı** (regresyon hedefi).

### Yaklaşım
1. **Ön işleme** — mikrobiyom öznitelikleri yaşlarla `Sample Accession` üzerinden birleştirilir; kimlik/yinelenen sütunlar atılır; eksik veri kontrol edilir.
2. **Öznitelik / hedef** — `X` = mikrobiyom bollukları, `y` = `Age`.
3. **Ölçekleme** — `StandardScaler`.
4. **Model** — eğitim/test ayrımıyla `RandomForestRegressor`.
5. **Değerlendirme** — **MAE** (yıl cinsinden ortalama mutlak hata) ve **R²**.

### Teknolojiler
`Python` · `pandas` · `numpy` · `scikit-learn`

### Çalıştırma
```bash
pip install pandas numpy scikit-learn matplotlib
jupyter notebook BiologicalAgePrediction.ipynb
```
`data.csv` ve `Ages.csv` dosyalarını notebook'un yanına koy ve tüm hücreleri çalıştır.
