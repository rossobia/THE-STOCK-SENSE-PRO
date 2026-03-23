# 📈 The Stock Sense PRO

Yapay zeka destekli, gerçek zamanlı küresel borsa, kripto ve döviz analiz terminali. Bu proje, finansal okuryazarlığı artırmak ve kullanıcılara karmaşık piyasa verilerini AI desteğiyle sadeleştirerek sunmak amacıyla geliştirilmiştir.

## 🚀 Canlı Demo Bağlantıları

Proje iki farklı sunucu altyapısında Sürekli Entegrasyon (CI/CD) ile canlıya alınmıştır. Cihazınıza veya ağ ayarlarınıza en uygun linkten projeyi test edebilirsiniz:

* 🟢 **Ana Sunucu (GitHub Pages):** [https://rossobia.github.io/THE-STOCK-SENSE-PRO/]
* 🔵 **Alternatif Sunucu (Cloudflare):** [https://the-stock-sense-pro.pages.dev]

## 🛠️ Kullanılan Teknolojiler ve Mimari

* **Ön Yüz (Frontend):** HTML5, CSS3, JavaScript (Tamamen Responsive - Mobil Uyumlu)
* **Grafik Motoru:** TradingView Lightweight Charts API
* **Yapay Zeka Motoru (Backend):** Google Gemini 2.5 Flash API
* **Sunucu & API Yönetimi:** Cloudflare Workers (CORS ve Cache yönetimi için özel yazılmış Serverless arka uç)
* **Veri Çekme (Scraping):** Yahoo Finance News API
* **CI/CD Pipeline:** GitHub & Cloudflare Pages entegrasyonu

## 🧠 Özellikler

* **Canlı Veri:** Küresel endeksler, BİST, Kripto ve Döviz piyasalarının anlık grafik takibi.
* **AI Destekli Yorumlama:** Aranan varlıkla ilgili son güncel haberlerin taranıp, profesyonel bir finansal analist ağzıyla (Kısa Özet, Temel Analiz, Beklenti ve Senaryolar) raporlanması.
* **Akıllı Hafıza (Cache):** API kotalarını korumak için Cloudflare Workers üzerinde yazılmış 10 dakikalık cache algoritması.
