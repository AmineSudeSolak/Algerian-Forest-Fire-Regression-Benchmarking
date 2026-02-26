Algerian Forest Fire — Regression & Regularization Study
Comparing Linear, Ridge, Lasso and ElasticNet after fixing data leakage and multicollinearity. Predicting Fire Weather Index (FWI) from meteorological measurements. This project focuses on understanding how data quality affects model behavior, not just achieving low error.

Project Motivation
Many beginner ML projects try different algorithms on clean datasets. This project does the opposite: Instead of changing the model, fix the data first. The goal is to observe how preprocessing decisions change regression behavior and stability.

What I Practiced
Handling real-world dirty data

Detecting and fixing multicollinearity

Preventing data leakage

Feature engineering based on dataset structure

Comparing regression regularization methods

Dataset Problem
The dataset contains measurements from two different climate regions, but the region label is missing as a feature. Because of this, the model initially learns averaged behavior instead of regional patterns. Additionally, several variables are mathematically derived from each other, causing:

Strong multicollinearity

Unstable regression coefficients

Unreliable interpretations

My Approach

Data Preparation
Reconstructed hidden region feature

Removed invalid observations

Fixed numeric data types

Converted fire labels to binary values

Standardized features using training data only

Feature Reliability
Highly correlated predictors were automatically removed using a correlation threshold. This reduces redundancy, coefficient instability and overfitting risk.

Models Compared
Linear Regression: Baseline behaviour

Ridge: Stabilize coefficients

Lasso: Automatic feature selection

ElasticNet: Combined regularization

All models tuned using 5-Fold Cross Validation.

Key Learnings
Data preprocessing impacted performance more than model choice

Multicollinearity breaks coefficient interpretability

Regularization improves model stability

Correct problem framing is more important than algorithm complexity

Tech Stack
Python, Pandas, NumPy, Scikit-Learn, Matplotlib, Seaborn

Project Structure
notebook.ipynb: full analysis & modeling workflow

data/: dataset

README.md: project documentation

Cezayir Orman Yangını — Regresyon & Regularization Çalışması
Linear, Ridge, Lasso ve ElasticNet modellerini data leakage ve multicollinearity giderildikten sonra karşılaştırma çalışması. Meteorolojik veriler kullanılarak Fire Weather Index (FWI) tahmini yapılmıştır. Bu proje düşük hata elde etmekten ziyade veri kalitesinin model davranışını nasıl etkilediğini anlamaya odaklanır.

Projenin Amacı
Birçok makine öğrenmesi projesi doğrudan model denemeye başlar. Bu projede yaklaşım tersidir: Modeli değiştirmek yerine önce veriyi düzelt. Amaç, ön işleme kararlarının regresyon stabilitesini nasıl etkilediğini gözlemlemektir.

Bu Projede Pratik Ettiklerim
Gerçek hayat verisi temizleme

Multicollinearity tespiti ve giderme

Data leakage önleme

Veri yapısına dayalı feature engineering

Regularization yöntemlerini karşılaştırma

Veri Setindeki Problem
Veri iki farklı iklim bölgesinden gelmektedir ancak bölge bilgisi özellik olarak verilmemiştir. Bu nedenle model başlangıçta bölgesel davranış yerine ortalama davranışı öğrenir. Ayrıca bazı değişkenler birbirinden türetildiği için:

Güçlü multicollinearity oluşur

Katsayılar kararsız hale gelir

Yorumlama güvenilirliği düşer

Uygulanan Yaklaşım
Veri Hazırlama
Gizli bölge değişkeni yeniden oluşturuldu

Hatalı gözlemler temizlendi

Veri tipleri düzeltildi

Yangın etiketi binary hale getirildi

Standardizasyon yalnızca eğitim verisi ile yapıldı

Özellik Güvenilirliği
Yüksek korelasyonlu değişkenler otomatik olarak kaldırıldı. Bu sayede gereksiz bilgi azaltıldı, katsayı stabilitesi arttı ve overfitting riski düştü.

Karşılaştırılan Modeller
Linear Regression: Temel davranış

Ridge: Katsayı stabilizasyonu

Lasso: Özellik seçimi

ElasticNet: Kombine regularization

Tüm modeller 5-Fold Cross Validation ile ayarlanmıştır.

Öğrenilenler

Performansı en çok veri ön işleme artırır

Multicollinearity yorumlanabilirliği bozar

Regularization modeli daha stabil yapar

Doğru problem kurmak modelden daha önemlidir

Kullanılan Teknolojiler

Python, Pandas, NumPy, Scikit-Learn, Matplotlib, Seaborn

Proje Yapısı

notebook.ipynb

data/

README.md
