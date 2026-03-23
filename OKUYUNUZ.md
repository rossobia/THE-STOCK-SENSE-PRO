# 📈 The Stock Sense PRO

Yapay zeka destekli, gerçek zamanlı küresel borsa, kripto ve döviz analiz terminali. Bu proje, finansal okuryazarlığı artırmak ve kullanıcılara karmaşık piyasa verilerini AI desteğiyle sadeleştirerek sunmak amacıyla geliştirilmiştir.

## 🚀 Canlı Demo Bağlantıları

Projenin ilk sürümü **Cloudflare Pages** (`.pages.dev` uzantısı) kullanılarak Sürekli Entegrasyon (CI/CD) hattı ile canlıya alınmıştır. Ancak yapılan saha testlerinde (8 farklı cihaz ve farklı ağlarda) erişilebilirlik oranının %50 seviyelerinde kaldığı tespit edilmiştir. 

**Sorunun Teknik Analizi:**
Türkiye'deki bazı İnternet Servis Sağlayıcılarının (ISP) ve mobil operatörlerin varsayılan "Güvenli İnternet" filtreleri ile üniversite/kurum ağlarının güvenlik duvarları, yeni oluşturulmuş `.dev` uzantılarını ve sunucusuz (serverless) alt alan adlarını zaman zaman şüpheli bularak DNS seviyesinde çözümleyememekte veya engellemektedir.

**Alınan Mimari Aksiyon:**
Projenin %100 kesintisiz erişebilmesini garanti altına almak amacıyla, DNS filtrelerine takılmayan **GitHub Pages** (`.github.io`) altyapısına geçiş yapılmıştır. Cloudflare sunucusu ise yedek (fallback) ortam olarak aktif tutulmaktadır.

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

### 📊 Bilgilendirme: Veri Sağlayıcı ve Grafik Kısıtlamaları

Projenin canlı grafik arayüzünde üçüncü parti finansal widget entegrasyonları (TradingView vb.) kullanılmaktadır. Testler sırasında özellikle **Borsa İstanbul (BİST)** hisselerinde veya bazı spesifik küresel varlıklarda grafiklerin ekrana yansımaması veya "Invalid Symbol" hatası alınması öngörülen bir durumdur.

**Durum Analizi:**
Bu durum uygulamanın kaynak kodlarından veya mimarisinden kaynaklanan bir hata (bug) **değildir**. Tamamen dış veri sağlayıcıların ücretsiz (Free Tier) paketlerde uyguladığı lisans politikaları, bölgesel borsa kısıtlamaları ve anlık veri kotaları ile ilgilidir. 

Sistem, bu tür dış veri kesintilerini tolere edebilecek şekilde tasarlanmıştır. Herhangi bir grafik API tarafından kısıtlansa ve ekranda yüklenmese dahi, arka plandaki yapay zeka (Gemini) haber okuma ve analiz etme motoru asenkron olarak çalışmaya ve kullanıcıya rapor sunmaya devam edecektir.
