# 🥗 AI Diyet Asistanı (Diet Q&A System)

Bu proje, önceden tanımlanmış diyet ve sağlık sorularını **Doğal Dil İşleme (NLP)** ve **Vektör Benzerliği (Semantic Search)** teknolojilerini kullanarak analiz eden ve en uygun cevabı bulan yapay zeka destekli bir uygulamadır.

Sistem, kullanıcı sorularını kelime bazlı değil anlamsal olarak eşleştirir. Ayrıca, tüm soru-cevap etkileşimlerini analiz amacıyla **Airtable** veritabanına otomatik olarak kaydeder.

## 🚀 Öne Çıkan Özellikler
* **Anlamsal Arama:** `SentenceTransformer` kullanarak soruları sayısal vektörlere dönüştürür ve anlam benzerliğine bakar.
* **Airtable Entegrasyonu:** Kullanıcı etkileşimlerini bulut tabanlı veritabanına loglar.
* **Hızlı ve Etkili:** Pandas ve Vektör uzayı hesaplamalarıyla anlık cevap üretir.

## 🛠 Kullanılan Teknolojiler
* **Python 3.x**
* **Sentence-Transformers:** (`all-MiniLM-L6-v2`) Metin vektörleştirme için.
* **Pandas:** Veri manipülasyonu.
* **Airtable API:** Loglama servisi.
* **Dotenv:** Güvenlik ve ortam değişkenleri.

## ⚙️ Kurulum ve Çalıştırma

**1. Gereksinimleri Yükleyin:**
```bash
pip install pandas sentence-transformers python-dotenv requests

AIRTABLE_TOKEN=your_airtable_token
BASE_ID=your_airtable_base_id
TABLE_NAME=Table 1

python main/main.py

Soru: Gece yemek yemek kilo aldırır mı?
>> Benzerlik Skoru: 0.99
>> Cevap: Gece geç saatlerde yemek yerseniz vücudunuzun sindirmesi zor olabilir...
(Airtable'a kaydedildi ✅)
