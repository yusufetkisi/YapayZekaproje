# CV ve İş İlanı Eşleştirme Projesi

Bu projede, CV (özgeçmiş) metinleri ile iş ilanlarını eşleştirmeyi amaçladım. Metin işleme teknikleri kullanarak, iki farklı veri kümesindeki içerikler arasında benzerlik skoru hesapladım. Böylece, her CV için en uygun iş ilanını belirlemeye çalıştım.

## Proje Dosya Yapısı

proje/
│
├── data/
│ ├── resume_data.csv # CV metinlerinin olduğu dosya
│ ├── postings.csv # İş ilanlarının bulunduğu dosya
│
├── output/
│ ├── cv_job_matches.csv # Eşleşme sonuçları
│
├── notebooks/
│ ├── main.ipynb # Tüm işlemlerin yapıldığı notebook
│
├── README.md # Bu tanıtım dosyası

markdown
Kopyala
Düzenle

## Kullandığım Yöntemler

- **Veri Ön İşleme:** Küçük harfe çevirme, noktalama işaretlerini temizleme, stopword çıkarma, lemmatizasyon ve stemming işlemleri uyguladım.
- **Vektörleme:** Metinleri TF-IDF yöntemiyle sayısal verilere dönüştürdüm.
- **Benzerlik Ölçümü:** Cosine similarity kullanarak CV ve iş ilanları arasında benzerlik oranı hesapladım.

## Veri Setleri

- CV verileri `career_objective` sütunundan alındı.
- İş ilanı verileri ise `description` sütununa dayanıyor.
- Metin dışındaki alanlar kullanılmadı.

## Çıktılar

Her CV için en uygun iş ilanı tespit edildi ve bu eşleşmeler `output/cv_job_matches.csv` dosyasına kaydedildi. Dosyada, eşleşen iş ilanı ile benzerlik skoru yer alıyor.

## Gereksinimler

Aşağıdaki kütüphaneleri yüklemek yeterli:

```bash
pip install pandas numpy scikit-learn nltk
Nasıl Çalıştırılır?
notebooks/main.ipynb dosyasını açın.

Hücreleri sırayla çalıştırın.

Sonuçlar otomatik olarak output klasörüne kaydedilir.

Notlar
Bu proje tamamen denetimsiz (unsupervised) bir yaklaşım içeriyor. Daha gelişmiş yöntemler (Word2Vec, BERT gibi) ileride eklenebilir.

Hazırlayan
Bu proje, yapay zekâ dersi kapsamında [Adını buraya yaz] tarafından geliştirilmiştir.

yaml
Kopyala
Düzenle

---

Bu haliyle daha samimi, anlaşılır ve “bir öğrenci yazmış” izlenimi veriyor.  
İsmini eklememi ister misin ya da istersen direk PDF’e dönüştürüp de verebilirim?







