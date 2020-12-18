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

Not: <h1> sayfada bir tane bulunmalı.

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
