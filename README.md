# Bi' Nakarat — Türkçe Pop Tahmin Oyunu

Tek dosyalık, internet gerektirmeyen kart oyunu. `index.html` dosyasını iPhone'da Safari ile açman yeterli.

## Nasıl oynanır

Destede **186 Türkçe pop kartı** var (90'lar → 2020'ler). Her kartta şarkı adı, sanatçı, dönem ve
oyun için yazılmış **iki satır ipucu** bulunur.

Üç mod:

| Mod | Ne olur |
|---|---|
| **İpucu Modu** | Şarkı adı bulanıktır. Alttaki iki satırı yüksek sesle okursun, diğerleri şarkıyı tahmin eder. Karta dokununca cevap açılır. |
| **Nakarat Modu** | Şarkı adı sende görünür, telefonu kimseye gösterme; nakaratı sen mırıldan/söyle, onlar bulsun. |
| **Açık Kart** | Her şey görünür, karışık liste gibi ilerlersiniz. |

- Dönem filtresi: 90'lar / 2000'ler / 2010'lar / 2020'ler
- Süre: süresiz, 60, 90 veya 120 saniye
- Tek grup veya 2 takım (takımlar sırayla oynar, sonunda kazanan çıkar)
- Kartı **sağa kaydır = bildi**, **sola kaydır = pas** (masaüstünde ok tuşları, boşluk = cevabı aç)
- Ayarlar tarayıcıda hatırlanır

## iPhone'a kurmak

1. Dosyayı telefona at (AirDrop / iCloud Drive / Dosyalar) ve Safari ile aç,
   ya da GitHub Pages'te yayınla.
2. Safari'de **Paylaş → Ana Ekrana Ekle** dersen tam ekran uygulama gibi açılır.

## Kart eklemek

`index.html` içindeki `SONGS` dizisine satır ekle:

```js
{t:"Şarkı Adı", a:"Sanatçı", d:"10", c:["Birinci ipucu satırı","İkinci ipucu satırı"]},
```

`d` alanı dönem: `"90"`, `"00"`, `"10"`, `"20"`.

## Not

Kartlardaki iki satır şarkı sözü değil, bu oyun için yazılmış tariflerdir; dönem etiketleri yaklaşıktır.
