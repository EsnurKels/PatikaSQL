# SQL SELECT

**SELECT** komutu ile veritabanından veri almak için kullanılan temel bir sorgudur.

### Kullanım Şekli

```
    SELECT tablo_sutunu, tablo_sutunu, ...
    FROM tablo_adi;
```

### Örnek 1 | Query
**_user_** tablosundan 'first_name' ve 'last_name' sütunlarını çağırmak için kullanılır.

```
    SELECT first_name, last_name
    FROM user;
```

### Örnek 2 | Query

**_actor_** tablosundaki tüm sütunları '*' karakteri ile çağırabiliriz.

```
    SELECT *
    FROM actor;
```
