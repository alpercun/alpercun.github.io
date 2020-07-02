---
title: "Flexbox"
date: "2020-07-02 21:00:00 +0300"
categories: [Blog]
tags: [CSS,Flexbox]
---

# `Flexbox`

Html css çalışırken zamanında sürekli ezbere yazdığım ve deneme yanılma yoluyla yaptığım bu  flexbox mantığını bir yazı haline getirip akılda kalıcı olması için bu bloğu yazıyorum. Referans aldığım video ve siteleri aşağıya döküman olarak ekleyeceğim. Buradan çıkardığım notlarla mantığını iyice kavradığımı düşünüyorum umarım sizin içinde aynı şekilde verimli bir yazı olur.

![flexbox](https://www.silocreativo.com/en/wp-content/uploads/2017/04/flexbox-cssgrid-practical-example.png)

# `Container için kullanılan özellikler`

![container](https://css-tricks.com/wp-content/uploads/2018/10/01-container.svg)

## `display: flex`

Bu özelliği verdiğimizde sayfada bulunan elemenlerin bulunduğu x ve y ekseninde esneklik özelliğini kullanarak yayılmasını sağlıyoruz. Bu kısımda `wrap` özelliği tarayıcıdan otomatik olarak `none` geliyor. None geldiğinden dolayı yatay eksende cisimlerimiz satır genişliği boyunca sığmaya zorlanıyorlar.

## `flex-wrap: wrap;`

Belirttiğimiz satır içerisinde konumlandırdığımız cisimlerin genişlikleri satır genişliğini aşarsa alt satıra konumlanarak cisimleri yerleştirmeye devam eder. Kısacası sarmalama işlemi yapar. 

![Flexbox%20584988916aee4494b841d14f7030cb2a/Ekran_Resmi_2020-06-30_20.16.05.png](Flexbox%20584988916aee4494b841d14f7030cb2a/Ekran_Resmi_2020-06-30_20.16.05.png)

## `flex-direction: row & flex-direction: column`

### `flex-direction: row`

Tarayıcı tarafından tanımlanan flex-direction özelliği `row` olarak gelir. Bu özellik sayesinde biz justify-content ve align-items özelliklerini normal şekilde kullanabiliriz. Justify-content yatay(x) ekseninde, Align-items ise dikey(y) ekseninde cisimleri hizalamak için kullanılır.


### `flex-direction: column`

Column özelliğini kullandığımız zaman x ve y ekseni justify-content ve align-items için yer değiştirir. Bunun sonucunda justify-content x ekseninde hizamala işlemini yaparken y ekseninde işlem yapmaya başlar. Aynı durum align-items içinde geçerli olup y ekseninde hizalama işlem yapmaya çalışırken  x ekseninde işlem yapmaya başlar. Bu yüzden flex-direction özelliği bizim için çok önemlidir.

![Flexbox%20584988916aee4494b841d14f7030cb2a/Ekran_Resmi_2020-06-30_20.24.32.png](Flexbox%20584988916aee4494b841d14f7030cb2a/Ekran_Resmi_2020-06-30_20.24.32.png)

## `justify-content`

Yatay eksende cisimleri hareket ettirmek için kullanılır. Tarayıcı tarafından tanımlanan flex-direction özelliği row olarak gelir. Eğer `flex-direction` özelliğini biz kendimiz column olarak getirirsek bu bize dikey eksende hareket etmemiz için sağlayan bir özellik olarak kullanmamızı sağlar. Bunun detaylı açıklaması flex-direction kısmında detaylıca açıkladım.

![Flexbox%20584988916aee4494b841d14f7030cb2a/Ekran_Resmi_2020-06-30_20.16.49.png](Flexbox%20584988916aee4494b841d14f7030cb2a/Ekran_Resmi_2020-06-30_20.16.49.png)

## `align-items`

Dikey eksende cisimleri hizalamak için kullanılır. Tabi `flex-direction: row;` ise ;)

![Flexbox%20584988916aee4494b841d14f7030cb2a/Ekran_Resmi_2020-06-30_20.17.29.png](Flexbox%20584988916aee4494b841d14f7030cb2a/Ekran_Resmi_2020-06-30_20.17.29.png)

## `align-content`

Bu bize birden fazla satırları hareket ettirmemizi sağlar align items'dan tek farkı budur. Bir diğer özellik ise `align-content` özelliğini kullandığımız anda `align-items'ın` hiçbir özelliği kalmıyor.

![Flexbox%20584988916aee4494b841d14f7030cb2a/Ekran_Resmi_2020-06-30_20.17.52.png](Flexbox%20584988916aee4494b841d14f7030cb2a/Ekran_Resmi_2020-06-30_20.17.52.png)

# `Items için kullanılan özellikler`

![Flexbox%20584988916aee4494b841d14f7030cb2a/Ekran_Resmi_2020-06-30_20.30.59.png](Flexbox%20584988916aee4494b841d14f7030cb2a/Ekran_Resmi_2020-06-30_20.30.59.png)

## `align-self`

Container içindeki boxların kendi başına hareket etmesini sağlar

![Flexbox%20584988916aee4494b841d14f7030cb2a/Ekran_Resmi_2020-06-30_20.34.10.png](Flexbox%20584988916aee4494b841d14f7030cb2a/Ekran_Resmi_2020-06-30_20.34.10.png)

## `flex-grow`

Eğer yerleştirdiğimiz elementlerin arasında boşluk varsa ve bizim seçtiğimiz bir elementin bu boşlukları doldurmasını istiyorsak bu özelliği kullanabiliriz. Bu özellik bize seçtiğimiz elementin boşlukları öncelikli olarak kendi hibesine eklenmesini sağlar.

![Flexbox%20584988916aee4494b841d14f7030cb2a/Ekran_Resmi_2020-06-30_20.37.24.png](Flexbox%20584988916aee4494b841d14f7030cb2a/Ekran_Resmi_2020-06-30_20.37.24.png)

## `flex-shrink`

flex-shrink özelliği verilen elemente bunun değeri yok bu artık sıkıştırılabilir diyoruz. Elemente verdiğimiz değer arttıkça sıkışma özelliği artar. Eğer seçtiğimiz elementin özelliğine 0 değerini verirsek bu kutu hiç sıkışmaz ve sadece geriye kalan kutular kendi aralarında anlaşıp eşit şekilde sıkışırlar.

![Flexbox%20584988916aee4494b841d14f7030cb2a/Ekran_Resmi_2020-06-30_20.42.18.png](Flexbox%20584988916aee4494b841d14f7030cb2a/Ekran_Resmi_2020-06-30_20.42.18.png)

![Flexbox%20584988916aee4494b841d14f7030cb2a/Ekran_Resmi_2020-06-30_20.42.29.png](Flexbox%20584988916aee4494b841d14f7030cb2a/Ekran_Resmi_2020-06-30_20.42.29.png)

![Flexbox%20584988916aee4494b841d14f7030cb2a/Ekran_Resmi_2020-06-30_20.42.43.png](Flexbox%20584988916aee4494b841d14f7030cb2a/Ekran_Resmi_2020-06-30_20.42.43.png)

## `order`

Elementler kendi aralarinda sıralıyken seçtiğimiz element'e verdiğimiz değer doğrultusunda sırada yerini alır. -1 ve 0 değerini verirsek en başa alır. Numaralandırma işlemi dizilerdeki 0. indeks kuralına göre yapılırsa kafa karışıklığı ortadan kalkar. 

1 Numaralı kutumuz 0. indeksteyken

![Flexbox%20584988916aee4494b841d14f7030cb2a/Ekran_Resmi_2020-06-30_20.50.51.png](Flexbox%20584988916aee4494b841d14f7030cb2a/Ekran_Resmi_2020-06-30_20.50.51.png)

1 numaralı kutumuz 3. indeksteyken

![Flexbox%20584988916aee4494b841d14f7030cb2a/Ekran_Resmi_2020-06-30_20.51.30.png](Flexbox%20584988916aee4494b841d14f7030cb2a/Ekran_Resmi_2020-06-30_20.51.30.png)

## Görsel Örnekleriyle beraber Flexbox mantığını anlamak için kaynak linkler

[**Codepen**](https://codepen.io/enxaneta/full/adLPwv)

[**CSS-TRICKS**](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)

## Referans aldığım video

Adem İlter [Her Derde Deva: CSS Flexbox](https://www.youtube.com/watch?v=_s15i3MoAyE)