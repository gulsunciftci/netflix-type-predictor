# 🎬 Netflix İçerik Türü Tahmini: Film mi, Dizi mi?

Bu proje, Netflix'in içerik açıklamalarını (descriptions) analiz ederek, bir içeriğin **"Movie" (Film)** mi yoksa **"TV Show" (Dizi)** mi olduğunu tahmin eden basit ama öğretici bir **makine öğrenmesi** uygulamasıdır.

Proje kapsamında doğal dil işleme (NLP), veri temizleme, vektörleştirme (TF-IDF) ve sınıflandırma (Logistic Regression) teknikleri kullanılmıştır.

---

## 📁 Kullanılan Veri Seti

Netflix Titles Dataset  
📥 Kaynak: [https://www.kaggle.com/datasets/shivamb/netflix-shows](https://www.kaggle.com/datasets/shivamb/netflix-shows)  
---

## 🛠️ Kullanılan Kütüphaneler

- `pandas`: Veri okuma ve işleme  
- `scikit-learn`: Model eğitimi ve değerlendirme  
- `TfidfVectorizer`: Metni sayısallaştırma (TF-IDF)  
- `train_test_split`: Veriyi eğitim/test olarak ayırma  
- `LogisticRegression`: Sınıflandırma modeli  
- `accuracy_score`: Doğruluk metriği hesaplama

---

## 🧪 Ne Yaptık?

### 🔹 1. Veriyi Temizledik
- Sadece `description` ve `type` sütunlarını aldık  
- Boş açıklamaları ve türleri sildik

### 🔹 2. Veriyi Ayırdık
- Açıklamaları (`X`) ve türleri (`y`) belirledik  
- Veriyi %80 eğitim, %20 test olarak böldük

### 🔹 3. Açıklamaları Sayıya Dönüştürdük (TF-IDF)
- Anlamsız kelimeleri çıkardık  
- En sık geçen 5000 kelimeyle açıklamaları vektörleştirdik

### 🔹 4. Modeli Eğittik (Logistic Regression)
- Eğitim verisiyle modeli eğittik  
- Metin özelliklerini tür tahmini için kullandık

### 🔹 5. Test Verisi ile Tahmin Yaptık
- Modelin başarısını test ettik  
- Tahminleri gerçek türlerle karşılaştırdık

### 🔹 6. Sonuçları Tablo Olarak Gördük
- Doğru ve yanlış tahminleri tablo hâlinde inceledik  
- Modelin ne kadar başarılı olduğunu gördük

---

## ✅ Model Performansı

- **Doğruluk (Accuracy):** %80 civarında  
- Model, açıklamalardan yola çıkarak türleri oldukça isabetli tahmin etti  
- Enformasyon içeriği yüksek açıklamalarda daha başarılı oldu

---

## 📊 Örnek Tahmin Tablosu

| Açıklama                                                 | Gerçek Tür | Tahmin   |
|----------------------------------------------------------|------------|----------|
| A haunted house with unexpected guests...                | Movie      | Movie    |
| A high school teen navigates friendships and breakups... | TV Show    | TV Show  |
| A war documentary told through archive footage...        | Movie      | TV Show  |

---

## 💡 Bu Projeden Ne Öğrendim?

- Makine öğrenmesiyle metin nasıl sınıflandırılır?  
- TF-IDF ile metni sayıya nasıl çevirebiliriz?  
- Eğitim/test ayrımı nasıl yapılır?  
- Basit bir modelle bile anlamlı tahminler yapılabilir  
- Modelin tahminlerini nasıl analiz ederiz?

---

## 🚀 Nasıl Çalıştırılır?

1. Gerekli kütüphaneleri yükleyin:
```pip install pandas scikit-learn ```
2. netflix_titles.csv dosyasını indirin ve proje klasörüne koyun.
3. Jupyter Notebook üzerinden adımları izleyin.
