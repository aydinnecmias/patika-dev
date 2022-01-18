### Aşağıdaki sorgu senaryolarını dvdrental örnek veri tabanı üzerinden gerçekleştiriniz.

<ol>
<li>Country tablosunda bulunan country sütunundaki ülke isimlerinden 'A' karakteri ile başlayıp 'a' karakteri ile sonlananları sıralayınız.
 </li>
<li>Country tablosunda bulunan country sütunundaki ülke isimlerinden en az 6 karakterden oluşan ve sonu 'n' karakteri ile sonlananları sıralayınız.
 </li>
<li>Film tablosunda bulunan title sütunundaki film isimlerinden en az 4 adet büyük ya da küçük harf farketmesizin 'T' karakteri içeren film isimlerini sıralayınız.
 </li>
 <li>Film tablosunda bulunan tüm sütunlardaki verilerden title 'C' karakteri ile başlayan ve uzunluğu (length) 90 dan büyük olan ve rental_rate 2.99 olan verileri sıralayınız.</li>
 </ol>

### Çözüm:

<ol>
<li><code>SELECT * FROM country WHERE country LIKE 'A%a';</code></li>
<li><code>SELECT * FROM country WHERE country LIKE '______%n';</code></li>
<li><code>SELECT * FROM film WHERE title ILIKE '%t%t%t%t%';</code></li>
<li><code>SELECT * FROM film WHERE title LIKE 'C%' AND length > 90 AND rental_rate = 2.99;</code></li>
 </ol>
