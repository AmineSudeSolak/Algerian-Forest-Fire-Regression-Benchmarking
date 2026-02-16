# Algerian-Forest-Fire-Regression-Benchmarking
Comparing Linear, Ridge, Lasso and ElasticNet after fixing data leakage and multicollinearity.
Algerian Forest Fire — Regression & Regularization

Predicting Fire Weather Index (FWI) from meteorological data using multiple regression models.

This project focuses on understanding how data quality affects model behaviour, not just achieving low error.

What I Practiced in This Project

Handling real-world dirty data

Detecting and fixing multicollinearity

Preventing data leakage

Feature engineering based on domain logic

Comparing regression regularization methods

Problem in the Dataset

The dataset contains measurements from two different climate regions, but the region label is missing as a feature.
Because of this, the model initially learns averaged behaviour instead of regional patterns.

Additionally, several variables are mathematically derived from each other, causing strong multicollinearity and unstable coefficients in linear regression.

My Approach

Reconstructed the hidden region feature

Cleaned invalid observations

Removed highly correlated predictors (correlation threshold)

Standardized features using training data only

Compared regression models

Models Compared
Model	Purpose
Linear Regression	Baseline
Ridge	Stabilize coefficients
Lasso	Feature selection
ElasticNet	Combined regularization

All models tuned using 5-Fold Cross Validation

Key Learnings

Data preprocessing impacted performance more than model choice

Multicollinearity breaks coefficient interpretability

Regularization improves model stability

Correct problem framing is more important than algorithm complexity

Tech Stack

Python · Pandas · NumPy · Scikit-Learn · Matplotlib · Seaborn

Project Structure
notebook.ipynb
data/
README.md

Goal of the Repository

Demonstrate a correct machine learning workflow:

Understand data → Fix data → Then model


Cezayir Orman Yangını — Regresyon & Regularization

Meteorolojik veriler kullanılarak Fire Weather Index (FWI) tahmini yapılmıştır.

Bu proje düşük hata elde etmekten ziyade veri kalitesinin model davranışını nasıl etkilediğini anlamaya odaklanır.

Bu Projede Pratik Ettiklerim

Gerçek hayat verisi temizleme

Multicollinearity tespiti ve giderme

Data leakage önleme

Mantıksal feature engineering

Regularization yöntemlerini karşılaştırma

Veri Setindeki Problem

Veri iki farklı iklim bölgesinden geliyor ancak bölge bilgisi özellik olarak verilmemiştir.
Bu yüzden model başlangıçta bölgesel davranışı değil ortalamayı öğrenir.

Ayrıca bazı değişkenler birbirinden türetildiği için güçlü multicollinearity oluşur ve doğrusal regresyon katsayıları kararsız hale gelir.

Yaklaşımım

Gizli bölge değişkenini yeniden oluşturma

Hatalı gözlemleri temizleme

Yüksek korelasyonlu değişkenleri kaldırma

Standardizasyonu sadece eğitim verisi ile yapma

Regresyon modellerini karşılaştırma

Karşılaştırılan Modeller
Model	Amaç
Linear Regression	Temel model
Ridge	Katsayı stabilizasyonu
Lasso	Özellik seçimi
ElasticNet	Kombine regularization

Tüm modeller 5-Fold Cross Validation ile ayarlanmıştır.

Öğrendiklerim

Performansı en çok veri ön işleme artırır

Multicollinearity yorumlanabilirliği bozar

Regularization modeli stabil yapar

Problemi doğru kurmak modelden daha önemlidir

Kullanılan Teknolojiler

Python · Pandas · NumPy · Scikit-Learn · Matplotlib · Seaborn

Proje Amacı

Doğru makine öğrenmesi iş akışını göstermek:

Veriyi anla → Veriyi düzelt → Sonra modeli kur
