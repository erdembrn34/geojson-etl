# GeoJSON ETL – İstanbul Otobüs Durakları

## 🔹 Proje Amacı
Bu proje, İstanbul Büyükşehir Belediyesi’nin açık veri portalından GeoJSON formatında paylaşılan otobüs duraklarını alıp **temizlemek, analiz etmek, görselleştirmek ve kaydetmek** amacıyla hazırlanmıştır.  
ETL (Extract, Transform, Load) süreci Jupyter Notebook içinde tamamen çalışacak şekilde tasarlanmıştır ve PostgreSQL gibi bir veritabanı gerektirmez.

---

## 🔹 Kullanılan Teknolojiler
- **Python 3**
- **GeoPandas**: Coğrafi veri işleme
- **Pandas**: Veri manipülasyonu
- **Matplotlib**: Statik görselleştirme
- **Folium**: İnteraktif harita oluşturma

---

## 🔹 Proje Özellikleri
- **Veri Çekme (Extract)**: GeoJSON formatındaki otobüs durak verisi internetten çekilir.  
- **Veri Temizleme (Transform)**:
  - Sadece gerekli kolonlar seçilir (`ID`, `ADI`, `DURAK_KODU`, `geometry`)
  - Geometri bilgisi olmayan satırlar çıkarılır
  - Metin verileri düzeltilir ve boşluklar temizlenir
- **Temel Veri Analizi**:
  - Toplam durak sayısı
  - Eksik değer kontrolü
  - Tekrarlayan ID’lerin kontrolü
- **Veri Yükleme (Load)**:
  - CSV ve GeoJSON formatında kaydedilir
  - Interaktif HTML harita oluşturulur
- **Görselleştirme**:
  - Statik harita (Matplotlib)
  - İnteraktif harita (Folium)

---

## 🔹 Kurulum

1. Repo’yu klonlayın veya ZIP olarak indirin:
```bash
git clone https://github.com/erdembrn34/geojson-etl.git
pip install -r requirements.txt
jupyter notebook notebooks/geojson-etl.ipynb
