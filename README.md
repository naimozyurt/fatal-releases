# Fatal

Windows için indirme programı: dosya, video ve torrent indirmeyi tek pencerede toplar, indirdiğini dönüştürür.
Bu repo yalnızca kurulum dosyalarını ve güncellemeleri barındırır; kaynak kod gizli repodadır.

## Kurulum

[Son sürümün](https://github.com/naimozyurt/fatal-releases/releases/latest) `Fatal-<sürüm>-setup.exe` dosyasını
indirip çalıştırın. `Fatal-<sürüm>-portable.exe` kurulumsuz çalışır ama kendini güncelleyemez ve tarayıcı
eklentisine bağlanamaz.

Kod imzası henüz olmadığı için Windows SmartScreen ilk açılışta uyarabilir: "Ek bilgi → Yine de çalıştır".

## Neler var

- **Dosya İndirici:** çok bağlantılı, kaldığı yerden süren indirme; tarayıcı indirmelerini devralır, sayfadaki
  dosyaları toplu indirir, süresi dolan indirme adresini yeniler, dosyaları türüne göre klasörlere koyar.
- **Video İndirici:** linkten video ya da ses; yalnızca bir bölümünü indirme, zamanlama, altyazı.
- **Torrent:** magnet ve `.torrent`, otomatik port açma, dosya seçimi, paylaşım sınırları.
- **Medya Dönüştürücü:** dönüştürme, küçültme, kesme, ses izleri, altyazı gömme, ekran kartıyla kodlama;
  indirme bitince kendiliğinden dönüştürme kuralları.
- Ortak hız sınırı, zamanlayıcı, "hepsi bitince uyku/kapat", önce hızlı diske indirip sonra taşıma,
  her yerden açılan komut paleti.

## Güncelleme

Fatal her açılışta yeni sürüm olup olmadığına bakar. Varsa menünün altında "Yeni sürüm" düğmesi çıkar:
tıklayınca indirir, kurar ve yeniden başlatır. "Otomatik güncelle" açıksa yeni sürüm arka planda iner ve
uygulamadan çıkınca kurulur.

## Tarayıcı eklentisi

"Fatal ile indir" eklentisi kurulumla gelir: Chrome / Edge → Uzantılar → Geliştirici modu → Paketlenmemiş öğe
yükle → `<kurulum klasörü>\resources\extension` (Fatal'da Dosya İndirici'de yolu ve "Klasörü aç" düğmesi var).
Yeni sürümden sonra uzantılar sayfasından yeniden yükleyin.

## Kullanım koşulları

Fatal yalnızca hakkına sahip olduğunuz ya da indirilmesine izin verilen içerik içindir: kendi dosyalarınız,
açık lisanslı içerik, yayıncısının indirmeye izin verdiği dosyalar. İndirilen içeriğin telif hakkına ve sitenin
kurallarına uymak kullanıcının sorumluluğundadır. Kopya korumalı (DRM) içerik indirilmez. Tam metin Fatal'da:
Ayarlar → Hakkında → Yasal.

## Açık kaynak

Fatal açık kaynak yazılımlar kullanır; liste Ayarlar → Hakkında → Yasal'da. İçinde gelen cobalt (AGPL-3.0)
değiştirilmiş kaynak koduyla birlikte kurulum klasöründe `resources\cobalt` altındadır (`LICENSE`, değişiklikler
`FATAL.md`). yt-dlp, FFmpeg ve aria2 ilk kullanımda kendi kaynaklarından indirilir.
