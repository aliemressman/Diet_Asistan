Diyet Soru-Cevap Sistemi

Bu proje, önceden tanımlanmış diyet sorularına benzerlik analizi yaparak en uygun cevabı bulan basit bir Türkçe Soru-Cevap uygulamasıdır. Kullanıcıdan gelen sorular, veri kümesindeki sorularla karşılaştırılır ve en benzer cevabı döndürür. Ayrıca, bu soru-cevap eşleşmeleri Airtable üzerinde kayıt altına alınır.

Kullanılan Teknolojiler

Python

Pandas: JSON veri kümesini düzenli bir DataFrame’e dönüştürmek için

Sentence-Transformers: Cümleleri sayısal vektörlere dönüştürmek ve benzerlik analizi yapmak için

Airtable API: Soru ve cevapların kayıt edilmesi için

dotenv: Gizli bilgilerin .env dosyasında saklanması için

Kurulum ve Çalıştırma

Gerekli kütüphaneleri yükleyin:

pip install pandas sentence-transformers python-dotenv requests

.env dosyası oluşturun:

Proje dizinine .env adlı bir dosya ekleyin ve aşağıdaki bilgileri girin:

AIRTABLE_TOKEN=your_airtable_token
BASE_ID=your_airtable_base_id
TABLE_NAME=Table 1

Projeyi çalıştırın:

python main/main.py

Nasıl Çalışır

Kullanıcının sorduğu soru, SentenceTransformer modeliyle sayısal bir vektöre çevrilir.

Veri setindeki tüm sorularla benzerliği hesaplanır.

En yüksek benzerlik puanı belli bir eşik değerini geçerse, cevap gösterilir.

Soru ve cevap bilgileri Airtable'a kaydedilir.

Örnek Kullanım

Diyet Soru-Cevap Sistemine Hoş Geldiniz
Çıkmak için 'q' yazın.

Sorunuzu yazın: Gece yemek yemek kilo aldırır mı?

En yakın soru: Gece yemek yemek kilo aldırır mı?
Benzerlik skoru: 0.99
Cevap: Gece geç saatlerde yemek yerseniz vücudunuzun sindirmesi zor olabilir ve bu kilo alımına neden olabilir.

Notlar

.env dosyasını asla GitHub gibi platformlarda paylaşmayın.

Eğer veri eklenmiyorsa, Airtable tablonuzda doğru alan adlarının (sorular, cevaplar) olduğundan emin olun.
