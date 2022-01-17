### Aşağıdaki sorgu senaryolarını dvdrental örnek veri tabanı üzerinden gerçekleştiriniz.

<ol>
<li>film tablosunda bulunan rental_rate sütunundaki değerlerin ortalaması nedir?
 </li>
<li>film tablosunda bulunan filmlerden kaç tanesi 'C' karakteri ile başlar?
 </li>
<li>film tablosunda bulunan filmlerden rental_rate değeri 0.99 a eşit olan en uzun (length) film kaç dakikadır?
 </li>
<li>film tablosunda bulunan filmlerin uzunluğu 150 dakikadan büyük olanlarına ait kaç farklı replacement_cost değeri vardır?
 </li>
 </ol>

### Çözüm:

<ol>
<li><code>select avg(rental_rate) from film;
limit 5 ;
</code></li>
<li><code>select count(*) from film
where title like 'C%';
</code></li>
<li><code>select max(length) from film
where rental_rate = 0.99;
</code></li>
<li><code>select count(distinct(replacement_cost)) from film
where length > 150;
</code></li>
 </ol>
