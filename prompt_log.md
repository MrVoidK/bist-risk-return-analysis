# Prompt Günlüğü

Bu dosya, proje geliştirme sürecinde kullanılan ana adım promptlarını kaydeder.

Bazı promptlar okunabilirlik için kısaltılmıştır, ancak gerçek istekleri ve geliştirme sırasını yansıtır.
Küçük yazım, biçim ve dil düzeltmeleri bu günlüğe eklenmez.

| No | Aşama | Kullanılan Prompt | Amaç |
|---|---|---|---|
| 1 | Proje iskeleti | "Create the initial repository structure for a BIST stock and TCMB exchange rate data science project. Add starter files such as README, requirements, prompt log, project instructions, and course requirements. Do not create the notebook or analysis yet." | Analize başlamadan önce düzenli proje yapısını oluşturmak. |
| 2 | Notebook iskeleti | "Create only the notebook outline in `notebooks/bist_tcmb_risk_return_analysis.ipynb`. Add Turkish markdown section titles and one basic import cell. Do not add data loading, EDA, visualization, or modeling code in this step." | Notebook yapısını veri işleme ve analiz adımlarından önce hazırlamak. |
| 3 | Veri yükleme akışı | "Add the data loading workflow to the notebook. Download selected BIST stock closing prices with yfinance and save them as raw data. Add a separate local CSV loading step for TCMB USD/TRY data from `data/raw/tcmb_usdtry.csv`. Do not clean, merge, visualize, calculate returns, or model yet." | BIST hisse verileri ve TCMB döviz kuru verisi için ham veri yükleme adımını hazırlamak. |
| 4 | Veri temizleme ve birleştirme | "Clean the raw BIST closing price data and TCMB USD/TRY data. Standardize date columns, check missing values, duplicate dates and data types, convert `usdtry_forex_buying` to numeric, rename it as `USDTRY_TCMB`, merge BIST and TCMB data by common dates, and save the cleaned price-level dataset. Do not calculate returns, create charts, or add modeling yet." | Ham BIST ve TCMB verilerini ortak tarih yapısında temiz ve analiz edilebilir hale getirmek. |
| 5 | Günlük getiri hesaplama | "Calculate daily percentage returns from the cleaned BIST and TCMB price-level dataset. Use `pct_change()`, rename return columns clearly, check missing values and data types, and save the processed return dataset. Do not create charts, answer research questions, or add modeling yet." | Farklı fiyat ölçeklerine sahip BIST hisseleri ve TCMB USD/TRY kuru için karşılaştırılabilir günlük getiri veri setini oluşturmak. |
| 6 | Çalıştırma kontrolü ve EDA | "Execute the notebook to check the data workflow and generated CSV files. Fix only minimal issues if needed. Then add EDA outputs, descriptive statistics, risk-return table, IQR-based outlier inspection, and required visualization types using the daily return dataset. Do not answer research questions or add modeling yet." | Önceki veri hazırlama adımlarının çalıştığını doğrulamak ve günlük getiri verisi üzerinden EDA ile görselleştirme bölümünü oluşturmak. |
