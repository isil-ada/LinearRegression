# Maaş Tahmini – Basit Doğrusal Regresyon

Bu proje, **deneyim (yıl)** ile **maaş ($)** arasındaki ilişkiyi basit doğrusal regresyon ile modelleyip tahmin etmeyi amaçlar. Çalışma bir Jupyter defteri (`linear-regression-salary-prediction.ipynb`) üzerinden yürütülmüştür.

## 🎯 Hedef
- Veri setini içe aktarmak ve hızlı bir EDA (head/info/eksik değerler/describe) yapmak  
- Veriyi eğitim/test olarak ayırmak  
- `LinearRegression` modeliyle eğitmek ve test verisi üzerinde tahmin yapmak  
- Gerçek ve tahmini değerleri aynı grafikte görselleştirmek

## 📦 Kullanılan Kütüphaneler
- `numpy`
- `pandas`
- `scikit-learn` (train_test_split, LinearRegression)
- `matplotlib`

> Gerekli paketleri hızlı kurulum için:
```bash
pip install -U numpy pandas scikit-learn matplotlib
```

## 📁 Dosyalar
- `linear-regression-salary-prediction.ipynb` – Tüm adımların bulunduğu Jupyter defteri

## 🗂️ Veri Seti
Notebook, Kaggle çalışma ortamındaki şu yolu kullanır:
```
/kaggle/input/salary-dataset-simple-linear-regression/Salary_dataset.csv
```
Aynı veri setine Kaggle üzerinden şu sayfadan erişebilirsiniz:  
**Salary Dataset – Simple Linear Regression**: https://www.kaggle.com/datasets/abhishek14398/salary-dataset-simple-linear-regression

> Not: Kaggle dışı yerel çalışmada CSV dosyasını indirip kendi klasör yolunuzu `pd.read_csv(...)` içine vermelisiniz.

## 🧪 Adım Adım İçerik
- **Veri Yükleme:** `pandas` ile CSV okunur.
- **EDA:** `head()`, `info()`, `isnull().sum()`, `describe()` vb. ile veri hızlıca incelenir.
- **Özellik/Hedef:** Genellikle `YearsExperience` → X, `Salary` → y olarak ayrılır.
- **Eğitim/Test Bölme:** `train_test_split(test_size=..., random_state=...)` ile ayrılır.
- **Model Eğitimi:** `LinearRegression().fit(X_train, y_train)`
- **Tahmin:** `model.predict(X_test)`
- **Görselleştirme:** Test noktaları (scatter) ve modelin çizgisi (line) aynı grafikte gösterilir.

## 📊 Örnek Grafik
Notebook sonunda **gerçek maaşlar** ile **tahmin edilen maaşların** karşılaştırıldığı bir çizim üretilir (yeşil noktalar & pembe çizgi).

## ⚠️ Notlar
- Veri seti küçük ve tek değişkenli olduğu için, model yalnızca doğrusal ilişkiyi yakalar. Gerçek dünyada maaşı etkileyen çok daha fazla değişken vardır.
- Reprodüksiyon için `random_state` parametresi sabitlenebilir.
- Kaggle’da çalışıyorsanız dosya yolu aynı kalmalı; yerelde çalışıyorsanız yolu güncelleyin.
