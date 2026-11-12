# Tsunami Atlası — Verisetleri

Tsunami Atlası notebook’unun farklı bilgisayarlarda dosya yüklemeden çalışması için kullanılan açık veri deposu.

| Dosya | Kullanım |
|---|---|
| `earthquake_1995-2023.csv` | Ana ham veri: 1.000 kayıt. Notebook mww filtresiyle 502 kaydı kullanır. |
| `external_events.json` | Eğitim/test dışında tutulan, kaynak bağlantılı 20 gerçek olay. |
| `provenance.json` | Ana veri kaynağı, sürümü, indirme zamanı ve SHA-256 bilgisi. |
| `ncei_external_sources.json` | Dış olay etiketleri için korunmuş NCEI kaynak kayıtları. |
| `earthquake_data.csv` | Projede tutulan ek/eski CSV; güncel model eğitiminde kullanılmaz. |

## Kaynaklar ve kullanım

Ana veri: [Kaggle Earthquake Dataset](https://www.kaggle.com/datasets/warcoder/earthquake-dataset), v3. Proje kaynak kaydı ana CSV için CC0 lisansını belirtir; ayrıntılar `provenance.json` içindedir.

Dış olay kaynakları: [USGS](https://earthquake.usgs.gov/fdsnws/event/1/) ve [NOAA NCEI](https://www.ncei.noaa.gov/products/natural-hazards/tsunamis-earthquakes-volcanoes/tsunamis). Her dış olayın kaynak bağlantısı ve etiket dayanağı JSON içinde korunur. Ana Kaggle etiketleri bağımsız katalogla yeniden doğrulanmamıştır. Dış negatiflerde NCEI kara içi deprem kaydında tsunami ilişkisi bulunmaması, bütün küçük dalgaların ölçülerek dışlandığı anlamına gelmez.

Notebook, yeniden üretilebilirlik için verileri belirli bir Git commit’ine sabitlenmiş `raw.githubusercontent.com` bağlantısından okur. Dosya seçmek veya giriş yapmak gerekmez; internet bağlantısı gerekir.

Canlı uygulama: https://tsunami-alert-system.netlify.app/
