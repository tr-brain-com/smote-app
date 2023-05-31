# smote

Genel olarak makine öğrenmesi modelleri sınıfların dengeli olmasını bekler. Bu durum, bir öğrenciden hem matematiği hem de geometriyi eşit derecede öğrenmesini istemek, ancak öğrenmesi için ona matematikte 100, geometride 5 çözülmüş örnek problem vermek gibidir. Bu durumu gerçek bir uygulama üzerinde görelim ve çözüm üretelim. Daha sonra bu çözümleri iyi bilinen 5-6 makine öğrenmesi algoritmasında test edelim ve sonuçları karşılaştıralım.

**Sihirli kelime “Smote” ve “Adasyn”**
Gerek Smote (Sysnthetic Minority Oversampling Technique) ve gerek Adaptif Sentetik (AdaSyn) makine öğrenmesi uygulamalarında (derin öğrenme ve her türlü model geliştirme aşamasından önce) sentetik veri üretimi yaparak sınıflar arasında ki dengesizliklerini gidermek ve model performansını iyileştirmek amacıyla yaygın olarak kullanılan kütüphanelerdir

Bir diğer ifadeyle, veri kümesindeki sınıf dağılımını dengelemek için bir aşırı örnekleme yöntemidir. Özellik uzayına yakın olan azınlık örneklerini seçer. Daha sonra özellikler uzayında örnekler arasına bir çizgi çizer ve bu çizgi boyunca bir noktada yeni bir örnek çizer.

Daha basit bir ifadeyle ise algoritma azınlık sınıfından rastgele bir örnek seçer ve K En Yakın Komşuyu kullanarak rastgele bir komşu seçer. Sentetik örnek, özellik uzayında iki örnek arasında oluşturulur.

Buraya kadar tanımlar üzerine farklı açılardan göz attıktan sonra şimdi gerçek bir örnekle testlerimizi yapalım. Veri üzerinde smote uygulanması sonucunda ne gibi farklılıklar oluşacağını da gözlemleyelim. 

# Hadi Başlayalım 

Smote uygulanması oldukça basittir. Öncelikle imbalanced-learn kütüphanesi sistemimizi kuruyoruz ediyoruz.

pip install imbalanced-learn

Kütüphaneyi sistemimize kurduktan sonra üzerinde işlem yapacağımız veri setini de sistemimizde hazır hale getirelim. Burada kullanacağım veri seti, “dermatology.csv” dosyası olacaktır. Veri seti 35 kolon ve 366 satırdan oluşmaktadır. Önce verimizi yükleyelim ve basit anlamda bir önişleme uygulayalım.

```python
data = pd.read_csv("dermatology_data.csv")
data.head(5)
```

Yazı serisinin tamamını okumak için [tıklayınız](https://www.brain-tr.com/dengesiz-verilerin-imbalanced-ustesinden-nasil-gelebiliriz/).

Notebook dosyası için [tıklayınız](https://github.com/tr-brain-com/smote-app/blob/main/smote_app.ipynb).
