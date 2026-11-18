# Kese — Gider Defteri

Kişisel harcamalarını kategorilere ayırıp takip edebileceğin, tarayıcıda çalışan, tek dosyalık bir gider defteri uygulaması. Kurulum, derleme veya sunucu gerekmez.

## Özellikler

- **Hesap sistemi:** kayıt ol / giriş yap. Kayıtta ülke, şehir, para birimi ve dil seçilir.
- **Gider takibi:** tarih, tutar, açıklama, kategori, ödeme yöntemi ve not; düzenleme, silme, arama ve kategori filtresi.
- **Kategoriler ve bütçe:** kendi kategorilerini renkle ekle, aylık bütçe koy; aşılınca uyarı gösterilir.
- **Aylık özet:** toplam, gider sayısı, günlük ortalama, kategori dağılımı (halka grafik) ve son 6 ayın karşılaştırması.
- **Gün gün takvim:** takvimde bir güne basınca o günün giderleri görünür.
- **Ülkene göre gelir sınıfı:** Dünya Bankası verileriyle (yoksulluk sınırları, Gini, gelir payları) gelirinin ülkendeki yeri tahmini olarak gösterilir. 171 ülke için veri vardır.
- **6 dil:** Türkçe, English, Deutsch, Français, Español, Русский. Ülke seçince dil önerilir.
- **Tüm dünya para birimleri**, ülkeye göre otomatik seçim.
- **CSV dışa aktarma** (Excel'de Türkçe karakterlerle açılır).
- Hareketli açılış sayfası ve "kendin dene" gelir sınıfı aracı.

## Çalıştırma

`index.html` dosyasını çift tıklayıp tarayıcıda aç. Hepsi bu.

İstersen yerel bir sunucuyla da açabilirsin:

```bash
npx serve .
```

## Veriler ve gizlilik

- Hesaplar ve giderler **yalnızca kendi tarayıcının `localStorage` alanında** saklanır. Sunucuya gönderilmez. Başka cihazda veya tarayıcıda hesap görünmez; tarayıcı verisini silersen kayıtlar da silinir.
- Parolalar düz yazı olarak değil, PBKDF2 (SHA-256, 150.000 tur) ile özetlenerek saklanır. Bu, gerçek bir sunucu tabanlı kimlik doğrulamanın yerini tutmaz; aynı bilgisayarı kullanan biri tarayıcı verilerine erişebilir.
- Sayfa şu dış kaynakları kullanır: Google Fonts (yazı tipleri) ve `countriesnow.space` (Türkiye dışındaki ülkelerin şehir listesi; yalnızca ülke bilgisi çekilir, kullanıcı verisi gönderilmez). İnternet yoksa şehir elle yazılabilir.
- Gelir sınıfı için gömülü veriler: [World Bank Open Data](https://data.worldbank.org/) (CC BY 4.0). Sınıflandırma, log-normal bir modele dayanan **kaba bir tahmindir**, kesin değildir. Ülkelerin kapsama özeti [`veri/ulke_verileri.csv`](veri/ulke_verileri.csv) dosyasındadır.

## Bilinen sınırlar

- Çok cihazlı hesap yok (sunucu gerekir). Plan: Supabase gibi bir arka uca taşımak.
- Çeviriler hızlı hazırlandı; ana dili olan biri gözden geçirmeli.
- Şehir listesi Türkiye için tam (81 il), diğer ülkelerde dış servisten gelir ve eksik olabilir.
- Gelir sınıfı hesabı için gelirin ülkenin kendi para biriminde girilmesi gerekir.

## Proje yapısı

```
index.html        Uygulamanın tamamı (HTML + CSS + JS)
veri/             Dünya Bankası verilerinin ülke bazlı özeti (CSV)
PRODUCT.md        Ürün bağlamı (kullanıcılar, amaç, ilkeler)
DESIGN.md         Tasarım sistemi notları
```

## Tasarım notu

Açılış sayfasının düzeni ve yazı stili [kesene.app](https://kesene.app/) sitesinden ilham alınarak farklı renklerle hazırlandı. Metinler, logo ve görseller bu projeye aittir; o siteden alınmamıştır. Kese ile Kesene ayrı ve ilgisiz projelerdir.

## Lisans

[MIT](LICENSE)
