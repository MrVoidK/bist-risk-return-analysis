# Prompt Günlüğü

Bu dosya, proje geliştirme sürecinde kullanılan ana adım promptlarını kaydeder.

Bazı promptlar okunabilirlik için kısaltılmıştır, ancak gerçek istekleri ve geliştirme sırasını yansıtır.
Küçük yazım, biçim ve dil düzeltmeleri bu günlüğe eklenmez.

| No | Aşama | Kullanılan Prompt | Amaç |
|---|---|---|---|
| 1 | Proje iskeleti | "Create the initial repository structure for a BIST stock and TCMB exchange rate data science project. Add starter files such as README, requirements, prompt log, project instructions, and course requirements. Do not create the notebook or analysis yet." | Analize başlamadan önce düzenli proje yapısını oluşturmak. |
| 2 | Notebook iskeleti | "Create only the notebook outline in `notebooks/bist_tcmb_risk_return_analysis.ipynb`. Add Turkish markdown section titles and one basic import cell. Do not add data loading, EDA, visualization, or modeling code in this step." | Notebook yapısını veri işleme ve analiz adımlarından önce hazırlamak. |
| 3 | Veri yükleme akışı | "Add the data loading workflow to the notebook. Download selected BIST stock closing prices with yfinance and save them as raw data. Add a separate local CSV loading step for TCMB USD/TRY data from `data/raw/tcmb_usdtry.csv`. Do not clean, merge, visualize, calculate returns, or model yet." | BIST hisse verileri ve TCMB döviz kuru verisi için ham veri yükleme adımını hazırlamak. |
