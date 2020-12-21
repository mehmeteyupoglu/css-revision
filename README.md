# CSS Notları

## Html Yapısı, Inline ve Block Elementler

- Div ve p ⇒ display: blocktur
- Inline elemana bazı özellikler tanımlanamaz: height gibi
- En çok kullanılan display stilleri: block, inline-block, inline
- Computed kısmı varsayılan değerleri ifade eder

## Semantik HTML ve CSS Yazma Yöntemleri

- Google’da SEO kaygısından dolayı semantik html tagleri kullanıyoruz.

## Basit Seçiciler

- CSS yukarıdan aşağıya doğru kod okuma yapar.
- => Bu seçici _universal selector_ olarak geçer. Sayfadaki herşeyi kapsar.
- Type seçici html elementlerini seçer.
- Class seçici ise html etiketlerine atanan classları seçer
- Id seçici ise sayfadaki tekil olan bir anahtarı seçer
- Attribute selector:

```css
[class] {
  color: red;
}
```

html etiketlerine atanan attribute'leri seçer.

Not: `<h1>` sayfada bir tane bulunmalı.

## Form Elemanları

- label input idsine göre ilerler
- eğer input labelın içine yazılırsa inputa id yazmaya gerek kalmaz
- input tiplerini text olarak bırakmamak gerekiyor. İlgili tipi yazmak daha doğru olur: email, tel, vb.
- radio butonlarda `name` mevcutsa butonlardan yalnızca birini seçer
- form etiketinin default methodu `get`tir
- form elemanlarının başarılı bir şekilde post işlemi yapabilmesi için `name`'i olması gerekiyor.
- formda görünmesini istemediğiniz dataları input type hidden olarak kodlayabiliriz.
- `display: inline` ise margin değerlerini almaz

## Box Sizing (Kutu Modeli)

- default değeri `content-box`tur
- sonrasında

```css
* {
  box-sizing: border-box;
}
```

olarak değiştirilmelidir.

## Reset.css ve Normalize.css - Sıfırdan HTML ve CSS Eğitimi

- Tarayıcı farklılıklarını ve ön tanımlı gelen Css ayarlarını sıfırlar
- Tarayıcı tarafından ön tanımlı gelen ayarlar `user agent stylesheet` altında yer alır. DevToolsta çalışırken buna dikkat etmek gerekir.
- Reset.css ön tanımlı gelen ayarları sıfırlar, normalize.css ise hepsini sıfırlamak yerine tarayıcı farklılıklarını ortadan kaldırır.
- Normalize daha yaygın kullanılıyor. CSS dosyalarınızın en üstüne aşağıdaki gibi dah'l edilmeli :

```css
@import https: //necolas.github.io/normalize.css/8.0.1/normalize.css;; ; ; ; ; ; ; ; ; ; ; ; ; ; ; ; ; ; ; ; ; ; ; ; ;
```

## Kısayol Tanımlamalar

- padding, margin gibi özellikler tanımlanırken kısayol tanımlama yapılabilir:

```css
padding-top: 10px;
padding-right: 20px;
padding-bottom: 10px;
padding-left: 30px;

/* Yukarıdaki kullanım yerine aşağıdaki gibi kısayol padding tanımlama yapılabilir.  */

padding: 10px 20px 10px 30px;

/* Bu şekildeki kısayol tanımlamalarını CSS saat yönünde okur. 

1. değer: yukarı
2. değer: sağa
3. değer: aşağı
4. değer: sola */
```

- aynı şekilde `border`, `background` gibi özelliklerde de kısayollar kullanılabilir. Detaylı bilgi için w3schools bakmalısınız.

## Renk Değerleri ve currentColor

- CSS3 ile birlikte 147 tane ön tanımlı renk ismi yazabiliyoruz.
- rgba => buradaki `a` alphayı temsil eder ve verdiğiniz değerin saydamlığını ayarlayabilirsiniz.

- mevcut color rengi border rengi olarak kullanılabilir(inheritance)
- `background-color: transparent` olarak kodladığımızda backgroundtaki rengi alabiliriz.

## Temel Ölçü Birimleri

- px => Verdiğiniz değer ne ise ekranda da aynı şekilde görünür

- em => Font size değeri
- rem => root em, kapsayıcıya bakmadan roottaki değere bakar
- % => kapsayıcının yüzdesi kadar
- vh
- vw
- vmin
- vmax

## Görünüm Özellikleri

- `display:none ` => Ekrana yüklenmez
- `visibility:hidden` => Ekrana yüklenir, görüntülenmez
- `opacity: 0` neredeyse `visibility:hidden` aynı duruma gelir

fotoğrafların görünümleri kapanmasına rağmen networke yüklenir (image lazy loading)
