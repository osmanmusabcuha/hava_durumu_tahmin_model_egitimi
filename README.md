# Transformatör Modelleri ile Hava Durumu Tahmini

## Genel Bakış
Bu proje, çoklu transformatör tabanlı modellerin İstanbul için hava durumu tahmini performansını değerlendirmektedir. Modeller, 2014-2024 yılları arasında Meteostat veri tabanından toplanan hava durumu verileriyle eğitilmiştir.

## Amaç
Bu çalışmanın amacı, modern derin öğrenme modellerinin meteorolojik parametreleri (sıcaklık, nem, rüzgar hızı gibi) hassas bir şekilde tahmin etme kapasitesini değerlendirmektir. ISTM, Transformer, Informer, TFT ve CNN gibi modeller karşılaştırılmış ve en etkili yöntem belirlenmiştir.

## Temel Özellikler
- **Veri Toplama**: 2014-2024 yılları arası hava durumu verileri Selenium kullanılarak Meteostat platformundan toplanmıştır.
- **Ön İşleme**: Veriler temizlenmiş, normalize edilmiş ve özellik mühendisliği uygulanmıştır.
- **Model Eğitimi**: Beş farklı modelin tahmin doğruluğu değerlendirilmiştir.
- **Performans Metrikleri**: RMSE, MAE, MAPE ve R² kullanılarak modellerin başarıları analiz edilmiştir.

## Değerlendirilen Modeller
1. **ISTM**: En düşük hata oranları ile en başarılı performans.
2. **Informer**: Uzun vadeli bağımlılıklar için etkili ancak genel doğruluk düzeyi düşüktür.
3. **Transformer**: Ortalama performans, genelleştirme sınırlarına sahiptir.
4. **CNN**: Kısa vadeli tahminlerde iyi performans, uzun vadede sınırlıdır.
5. **TFT**: Dengeli ve stabil performans.

## Sonuçlar
- **ISTM**: En düşük hata oranları ile tüm modelleri geride bıraktı.
- **TFT**: Dengeli ve stabil, çoklu ufuk tahminleri için uygun.
- **Informer**: Büyük veri setlerinde potansiyel sunuyor.

## Sınırlılıklar
- Veri kapsamı sadece İstanbul ile sınırlıdır.
- Hesaplama maliyetleri nedeniyle geniş kapsamılı deneyler sınırlı tutulmuştur.
- Aşırı hava olayları üzerine daha fazla test gerekmektedir.

## Gelecek Çalışmalar
- Veri setini daha geniş bölgeleri içerecek şekilde genişletmek.
- Hibrit modeller geliştirerek istatistiksel ve derin öğrenme yöntemlerini birleştirmek.
- Daha fazla meteorolojik parametrenin tahminlere dahil edilmesi.

## Nasıl Çalıştırılır
1. Reponun bir kopyasını klonla:
    ```bash
    git clone https://github.com/kullaniciadi/weather-forecasting.git
    ```
2. Gerekli bağımlılıkları yükle:
    ```bash
    pip install -r requirements.txt
    ```
3. Veri setini hazırla (`data` klasöründe detaylar bulunmaktadır).
4. Model eğitim skriptini çalıştır:
    ```bash
    python train_model.py
    ```
5. Sonuçları `results` klasöründe görüntüle.

## Atıf
Bu projeyi kullanırsanız lütfen aşağıdaki gibi atıfta bulunun:
> Malkoc, E., & Cuha, M. O. (2024). Transformatör Modelleri ile Hava Durumu Tahmini.

---
Daha fazla bilgi için [rapor](./10_Rapor.pdf) dosyasına bakınız.
