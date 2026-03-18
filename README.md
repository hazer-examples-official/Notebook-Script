# 📒 Not Defteri — Hazer Örnek Betiği

Basit bir komut satırı not uygulaması. Not ekleme, silme, listeleme ve arama işlemlerini Hazer sözdizimiyle gerçekleştirir.

## Özellikler

- Not ekleme ve silme
- Tüm notları listeleme
- Anahtar kelimeyle not arama (`icerir_mi` yardımcı fonksiyonu ile)
- Hata yönetimi (`dene / yakala / nihayet`)

## Kullanılan Hazer Sözdizimi

| Kategori | Kullanılan |
|---|---|
| Fonksiyon | `işlev` |
| Koşul | `eğer` / `değilse` |
| Döngü | `ozyinele` / `içinde` |
| Liste metodları | `ekle`, `cikar`, `kopyala` |
| Hata yönetimi | `dene`, `yakala`, `nihayet` |
| Doğrulama | `teyit` |
| Dönüş | `dondür` |
| Sabitler | `Dogru`, `Yanlis` |

## Teknik Not

Python'un membership `in` operatörü (`x in y`) Hazer v0.3.0'da expression katmanında henüz Türkçe karşılık almadığından, arama işlevi `icerir_mi()` adlı özel bir yardımcı fonksiyonla yazılmıştır. Bu fonksiyon, string dilim karşılaştırması (`metin[i:i+n]`) ile `aralik` ve `uzunluk` kullanarak tamamen Hazer sözdizimiyle üyelik testi yapar.

## Çalıştırma

```bash
/path/to/hazer/python notebook.hazer
```

## Örnek Çıktı

```
✅ Not eklendi: 'Marketten süt al'
✅ Not eklendi: 'Projeyi teslim et'
📒 Notlarım:
  [0] Marketten süt al
  [1] Projeyi teslim et
🔍 2 sonuç:
   → Marketten süt al
   → Marketten ekmek al
🗑️  Silindi: 'Marketten süt al'
   (Kalan not sayısı: 3)
```
