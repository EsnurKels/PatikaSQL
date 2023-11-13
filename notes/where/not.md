# SQL WHERE

(ko) --> Karşılatırma operatörü anlamına gelmektedir.

SELECT komutuyla çağırdığımız verileri belirli bir koşula göre çekmek istediğimizde WHERE komutunu kullanırız.

### Kullanım Şekli

```
    SELECT tablo_sutunu, tablo_sutunu,...
    FROM tablo_name
    WHERE tablo_sutunu =(ko) koşul_durumu;
```

WHERE sonrasında koşul belirtilicek sütuna karışalştırma operatörlerinden biri kullanılır ve koşul yazılır. (ör. meyve_adi = 'Elma' veya ort >= 50 vb.)

### Örnek 1 | Query

**_urunler_** tablosunda **_urun_adi_** 'Kalem' olanların gelmesini istiyor.

```
    SELECT urun_adi
    FROM urunler
    WHERE urun_adi = 'Kalem';
```

### Örnek 2 | Query

**_film_** tablosundaki **_imbd_** sütunundan 5 eşit veya büyük olanları çağırmasını istiyor.

```
    SELECT film_adi, imdb
    FROM film
    WHERE imdb >= 5;s
```


### MATIKSAL OPERATÖRLERİN KULLANIMI

WHERE koşulu içinde yazılan koşul durum birden fazla koşulla karşılaştırmak için mantıksal operatörleri kullanırız. (AND, OR ve NOT)

#### AND Operatörü

**AND** operatörü tüm yazılan koşulların true olaması durumda verileri getirir.
Eğer bir koşul false olarak dönerse bu koşul çalışmaz.

**Kullanım Şekli**

```
    SELECT tablo_sutunu, ...
    FROM tablo_adi
    WHERE tablo_sutunu =(ko) kosul AND tablo_sutunu >(ko) kosul
```

**Örnek 1 | Query**

```
    SELECT *
    FROM departmanlar
    WHERE departman_adi = 'IT' AND is_kimligi= 'Developer';
```


#### OR Operatörü

**OR** operatörü çalışması için koşullardan en az birtanesinin true dönmesi yeterlidir.

**Kullanım Şekli**
```
    SELECT tablo_sutunu, ...
    FROM tablo_adi
    WHERE tablo_sutunu =(ko) kosul OR tablo_sutunu =(ko) kosul
```

**Örnek 1 | Query**

**_departman_** tablosundaki **_departman_adi_** sutunun IT veya HR olduğunu kontrol edip verileri tüm verileri çağırır.

```
    SELECT *
    FROM departmanlar
    WHERE departman_adi = 'IT' OR departman_adi= 'HR';
```


#### NOT Operatörü

**NOT** operatörü koşulu tersine çevirmek için kullanılan bir operatördür.

**Kullanım Şekli**
```
    SELECT tablo_sutunu, ...
    FROM tablo_adi
    WHERE NOT tablo_sutunu =(ko) kosul
```

**Örnek 1 | Query**

**_departman_** tablosundaki **_departman_adi_**, 'Finance' olmayanları çağırmak için kullanılmıştır.

```
    SELECT *
    FROM departmanlar
    WHERE NOT departman_adi = 'Finance';
```