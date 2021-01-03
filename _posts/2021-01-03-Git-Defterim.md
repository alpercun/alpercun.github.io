---
title: "Git Notları"
date: "2021-01-03 21:24:00 +0300"
categories: [Blog]
tags: [Git]
---

# `Yardımcı Git Komutları`

![](/assets/img/sample/git-notes.png)

Bu yazımda open source projelere katkı sağlarken veya kendi projelerimde bir değişiklik yapmak istediğimde sürekli kafamı karıştıran `git komutlarının` nasıl ve hangi durumlarda kullandığımı elimden geldiğince atmaya çalışacağım.

---

Git'i herhangi bir projemizde kullanabilmemiz için önce giti çağırmamız gerekiyor yani versiyonlamamız gerekiyor. Git sayesinde projedeki değişikliklerimizi bu şekilde tutabiliriz ve kayıt edebiliriz.

```console
  $ git init
```

---

Projede yapılan değişiklikleri eklememiz için

```console
  $ git add .
```

veya

```console
  $ git add <dosyaAdı>
```

---

Yapılan değişiklikleri metinsel olarak ifade etmek için

```console
  $ git commit -m "Yapilan degisiklikler"
```

---

Projenin istenilen halini göndermek için

```console
  $ git push
```

---

Projede atılmış bütün commitleri görmek için

```console
  $ git log
```

---

Gönderdiğimiz projede değişiklik oldu ve son halini geri almak istiyorsak

```console
  $ git pull
```

---

Main'den çıkıp yeni bir branch üzerine geçiş yapmak istersek

```console
  $ git checkout -b <branch-adi>
```

yada

```console
  $ gco -b <branch-adi>
```

---

Branch'den çıkıp main üzerine geçiş yapmak istersek

```console
  $ git checkout main
```

yada

```console
  $ gco main
```

---

Projede değişiklik yapılan dosyaları görmek için

```console
  $ git status
```

ya da

```console
  $ gst
```

---

Eski commitlere geri dönmek istersek

```console
  $ git checkout <hashcode ilk 6 hane veya hepsi>
```

---

Tekrar son commitimize geri dönmek istersek

```console
  $ git checkout master
```

---

-Projede **commit** atmış fakat yapılan değişiklikleri **puslamamış** bir durumda olduğum anlarda;

> Girilen commit'i iptal etmek ve commit'te yapılan değişikliklerin hepsini silmek için

```console
  $ git reset --hard HEAD~1
```

> Son atılan commit'i iptal etmek ve commit içindeki değişiklikleri tekrar görmek için

```console
  $ git reset --soft HEAD~1
```

> Yazdığımız commit mesajını yanlış girdik ve bunu değiştirmek istiyoruz

```console
  $ git commit --amend
```

.
.
.
.
.
Eklenecek

# `Kaynaklar`

[**Basic Git Commands**](https://confluence.atlassian.com/bitbucketserver/basic-git-commands-776639767.html)

[**Rewriting History**](https://www.atlassian.com/git/tutorials/rewriting-history)
