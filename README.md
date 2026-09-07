# Bi' Nakarat — Türkçe Pop Tahmin Oyunu

Tek dosyalık, internet gerektirmeyen kart oyunu. `index.html` dosyasını iPhone'da Safari ile açman yeterli.

## Nasıl oynanır

Destede **186 Türkçe pop kartı** var (90'lar → 2020'ler). Her kartta şarkı adı, sanatçı, dönem ve
kartın altında **iki satır** bulunur. Bu iki satırı istediğin metinle sen doldurursun
(bkz. *Söz satırlarını kendin gir*); doldurmadığın kartlar hazır ipucu satırlarıyla oynanır.

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

## Söz satırlarını kendin gir

Ana ekranda iki düğme var:

**Kartları düzenle** — 186 kartın listesi. Bir karta dokun, alttaki iki satıra ne yazarsan
kartta o görünür. `+` ile destede olmayan yeni şarkı da ekleyebilirsin.

**İçe / dışa aktar** — toplu doldurmak için. Her satıra bir kart gelecek şekilde yapıştır:

```
Şarkı Adı | Sanatçı | 1. satır | 2. satır
Kuzu Kuzu | Tarkan | ... | ...
```

- Destede zaten olan bir şarkıyı yazarsan sadece satırları güncellenir, kart ikilenmez.
- Destede olmayan bir şarkı yazarsan yeni kart olarak eklenir (dönemini o ekrandaki
  düğmelerden seçersin).
- Aynı ekrandaki **yedek** kutusu, girdiğin her şeyin JSON hâlidir. Kopyalayıp saklarsan
  başka bir telefonda yapıştırıp "Yedeği geri yükle" ile aynı desteyi kurabilirsin.

Girdiğin satırlar sadece o telefonun tarayıcısında (localStorage) durur, dosyaya yazılmaz.

**Sadece sözlü kartlar** düğmesini açarsan tur yalnızca kendi satırlarını girdiğin kartlardan kurulur.

## Kod içinden kart eklemek

`index.html` içindeki `SONGS` dizisine satır ekle:

```js
{t:"Şarkı Adı", a:"Sanatçı", d:"10", c:["Alt satır 1","Alt satır 2"]},
```

`d` alanı dönem: `"90"`, `"00"`, `"10"`, `"20"`.

## Not

Kutudan çıkan hâliyle kartlardaki iki satır şarkı sözü değil, oyun için yazılmış tariflerdir;
o satırları kendi metninle değiştirmek sana kalmış. Dönem etiketleri yaklaşıktır.
