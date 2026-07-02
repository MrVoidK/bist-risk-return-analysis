# BIST Hisseleri ve TCMB Döviz Kuru Verileriyle Risk-Getiri Analizi

## Proje Bilgileri

- Öğrenci Adı Soyadı: Ömer KANDUROL
- Öğrenci Numarası: 1306240077
- Ders: Veri Bilimi
- Tema: Finans & Ekonomi — BIST hisse verileri, TCMB döviz kurları

## Proje Amacı

Bu proje, seçilmiş BIST hisseleri ile TCMB USD/TRY döviz kuru verilerini kullanarak temel bir veri bilimi iş akışını uygulamayı amaçlamaktadır.

Çalışma; günlük getiriler, volatilite/risk, korelasyonlar, araştırma soruları ve basit bir regresyon modeli üzerine odaklanır.

Proje eğitim amacıyla hazırlanmıştır ve yatırım tavsiyesi değildir.

## Kullanılan Finansal Varlıklar

- THYAO.IS
- ASELS.IS
- GARAN.IS
- SISE.IS
- KCHOL.IS
- TCMB USD/TRY döviz alış kuru (`USDTRY_TCMB`)

## Veri Kaynağı ve Kullanım Notu

- BIST hisse fiyatları, `yfinance` kütüphanesi aracılığıyla Yahoo Finance üzerinden alınmıştır.
- USD/TRY döviz kuru verisi, TCMB günlük döviz kuru verilerinden elde edilmiştir.
- Veriler yalnızca eğitim ve analiz amacıyla kullanılmıştır.
- Veri sağlayıcılarının kullanım koşulları geçerlidir; bu proje veri sağlayıcıları tarafından onaylanmış resmi bir çalışma değildir.

## Tarih Aralığı

Planlanan tarih aralığı:

- 2022-01-01 — 2026-06-30

Takvim ve işlem günü farkları nedeniyle ortak veri setindeki ilk ortak iş günü `2022-01-03` olabilir.

## Proje Dosya Yapısı

```text
data/
  raw/
  processed/
notebooks/
reports/
README.md
prompt_log.md
requirements.txt
```

## Kullanılan Kütüphaneler

- pandas
- numpy
- matplotlib
- seaborn
- yfinance
- scikit-learn
- jupyter
- nbformat
- nbconvert

## Kurulum

```bash
pip install -r requirements.txt
```

## Notebook Nasıl Çalıştırılır?

1. Jupyter Notebook veya VS Code ile `notebooks/bist_tcmb_risk_return_analysis.ipynb` dosyasını açıp `Run All` çalıştırılabilir.

2. Terminal üzerinden aşağıdaki komut kullanılabilir:

```bash
jupyter nbconvert --to notebook --execute notebooks/bist_tcmb_risk_return_analysis.ipynb --inplace --ExecutePreprocessor.timeout=900
```

## Üretilen Dosyalar

- `data/raw/bist_close_prices_raw.csv`
- `data/raw/tcmb_usdtry.csv`
- `data/processed/clean_price_data.csv`
- `data/processed/daily_return_data.csv`

## Araştırma Soruları

1. Seçilen BIST hisselerinin günlük getiri dağılımları nasıldır?
2. Hangi hisse daha yüksek risk/volatilite göstermektedir?
3. TCMB USD/TRY kuru ile BIST hisselerinin günlük getirileri arasında güçlü bir ilişki var mıdır?
4. Seçilen BIST hisseleri birbirleriyle benzer hareket ediyor mu?

## Modelleme

Projede basit ve açıklanabilir bir Linear Regression modeli kullanılmıştır.

- Hedef değişken: `THYAO_Return`
- Özellik değişkenleri: `ASELS_Return`, `GARAN_Return`, `SISE_Return`, `KCHOL_Return`, `USDTRY_Return`
- Değerlendirme metrikleri: MAE, RMSE, R²

Modelin amacı yatırım tahmini yapmak değil, veri bilimi iş akışındaki temel modelleme adımını göstermektir.

## Sınırlamalar

- Yalnızca seçilen beş BIST hissesi analiz edilmiştir.
- Dış makro-finansal değişken olarak yalnızca USD/TRY döviz kuru kullanılmıştır.
- Günlük finansal getiriler gürültülü ve tahmin edilmesi zor olabilir.
- Korelasyon nedensellik anlamına gelmez.
- Şirket haberleri, finansal tablolar, faiz oranları, enflasyon ve küresel piyasa göstergeleri analize dahil edilmemiştir.

## Yatırım Tavsiyesi Değildir

Bu proje yalnızca eğitim amacıyla hazırlanmıştır. Buradaki analizler yatırım tavsiyesi değildir.

## Teslim Dosyaları

- `notebooks/bist_tcmb_risk_return_analysis.ipynb`: Çalışır Jupyter Notebook
- `reports/rapor.pdf`: Kısa proje raporu
- `prompt_log.md`: Prompt günlüğü
- `README.md`: Proje açıklaması ve çalıştırma talimatları