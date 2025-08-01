# E-Ticaret Ürün Yorumlarından Duygu Analizi ve Sınıflandırma

🌟 Proje Amacı

Bu projede, bir e-ticaret platformunda yer alan 15.000+ adet ürün yorumu analiz edilerek; kullanıcıların olumlu, olumsuz ve nötr yorumlarının yapısı çözümlemeye çalışılmıştır. Doğal dil işleme (NLP) teknikleriyle metin temizleme, özellik çıkarma ve istatistiksel analizler yapılarak; son aşamada yorumun metnine bakarak duygu tahmini yapabilen bir makine öğrenmesi modeli kurulmuştur.

❓ Ana Sorular

Kullanıcılar hangi duygularla yorum yazıyor?

Olumsuz yorumlar yapısal olarak olumlu yorumlardan farklı mı?

En sık kullanılan kelimeler neler?

Duygu tahmini yapan bir model ne kadar başarılı olur?

📊 Veri Seti

Veri seti, "Metin" ve "Durum" olmak üzere iki sütundan oluşmaktadır:

Metin: Ürün yorumu metni

Durum: 0=Olumsuz, 1=Olumlu, 2=Nötr

🔄 Ön İşlemler:

Eksik veriler temizlendi.

Yorum uzunlukları (karakter ve kelime bazlı) hesaplandı.

TF-IDF ile metinler sayısallaştırıldı.

📊 Analizler ve Gözlemler

🔎 Genel Durum Dağılımı

Toplam yorumların %88’i olumlu, %9’u olumsuz, %3’ü nötr.

Olumsuz yorumlar ortalama olarak daha uzundur. Şikayet içeren yorumlar daha detaylı yazılmaktadır.

💡 WordCloud Analizi

Olumlu yorumlarda "harika", "kaliteli", "hızlı" gibi memnuniyet bildiren kelimeler sık kullanılmıştır.

Olumsuz yorumlarda "bozuk", "iade", "geç geldi" gibi ifadeler öne çıkmıştır.

📊 Yorum Uzunluğu İstatistikleri

Olumsuz yorumlarda ortalama uzunluk 87 karakter, olumlu yorumlarda 60 karakter civarındadır.

Medyan değerler de benzer şekilde dağılım farklılığını desteklemektedir.

🧠 Makine Öğrenmesi ile Duygu Sınıflandırması

TF-IDF ile 5000 kelimeye kadar özellik çıkarıldı.

Logistic Regression modeli eğitildi.

Veri %80 eğitim, %20 test olarak bölündü.

📊 Model Performansı

Accuracy: %88.99

F1-skorlar:
- Olumlu: 0.92
- Olumsuz: 0.92
- Nötr:    0.51

Model, olumlu ve olumsuz yorumları ayırt etmede başarılıdır.

Nötr yorumlar sınırda kaldığı için çoğu zaman yanlış sınıflandırılmıştır.

📊 Sonuç ve Öneriler

E-ticaret platformlarında şikayet içerikli yorumlar genellikle daha uzun ve detaylıdır.

WordCloud analizi ile markalara dönüt verebilecek anahtar kelimeler tespit edilebilir.

Basit bir TF-IDF + Logistic Regression modeliyle %89 başarıyla duygu tahmini yapılabilmektedir.

Nötr yorumların daha net tanımlanabilmesi için ek özellik üretimi ve verinin genişletilmesi faydalı olabilir.

🔍 Görsellerden Örnekler

Yorumların duygu dağılımı

Olumlu/Olumsuz WordCloud

Yorum uzunluğu histogramı

Confusion Matrix

🔗 Kullanılan Kütüphaneler

pandas, seaborn, matplotlib

wordcloud, scikit-learn
