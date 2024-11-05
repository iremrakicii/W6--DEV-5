# SQL Sorguları Açıklaması

Bu dosya, belirli SQL sorgularını açıklamak için hazırlanmıştır. Her sorgu, veritabanından bilgi çekmek amacıyla tasarlanmıştır.

### 1. Soru

```sql
SELECT title, length FROM film
WHERE title ILIKE '%n'
ORDER BY length DESC
LIMIT 5;
```
Bu sorgu, film tablosundan başlığı "n" harfi ile biten filmleri seçer (ILIKE kullanımı büyük/küçük harf duyarlılığını yok sayar). Sonuçları film uzunluğuna göre azalan sırayla sıralar ve en uzun 5 filmi getirir.

### 2. Soru
```sql
SELECT title, length FROM film
WHERE title ILIKE '%n'
ORDER BY length ASC
OFFSET 5
LIMIT 5;
```
Bu sorgu, yine film tablosundan başlığı "n" harfi ile biten filmleri seçer ve sonuçları film uzunluğuna göre artan sırayla sıralar. İlk 5 sonucu atlar (OFFSET 5) ve sonraki 5 filmi getirir.

### 3. Soru
```sql
SELECT last_name FROM customer
WHERE store_id = 1
ORDER BY last_name DESC
LIMIT 4;
```
Bu sorgu, customer tablosundan store_id değeri 1 olan müşterilerin soyadlarını seçer. Sonuçları soyada göre azalan sırayla sıralar ve en üstteki 4 soyadı getirir.
