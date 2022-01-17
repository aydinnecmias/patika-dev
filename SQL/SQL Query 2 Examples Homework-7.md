### Aşağıdaki sorgu senaryolarını dvdrental örnek veri tabanı üzerinden gerçekleştiriniz.

<ol>
<li>film tablosunda bulunan filmleri rating değerlerine göre gruplayınız.
 </li>
<li>film tablosunda bulunan filmleri replacement_cost sütununa göre grupladığımızda film sayısı 50 den fazla olan replacement_cost değerini ve karşılık gelen film sayısını sıralayınız.
 </li>
<li>customer tablosunda bulunan store_id değerlerine karşılık gelen müşteri sayılarını nelerdir? 
<li>city tablosunda bulunan şehir verilerini country_id sütununa göre gruplandırdıktan sonra en fazla şehir sayısı barındıran country_id bilgisini ve şehir sayısını paylaşınız.
 </li>
 </ol>

### Çözüm:

<ol>
<li><code>select rating, count(*) from film
group by rating;
</code></li>
<li><code>select replacement_cost, count(*) from film
group by replacement_cost
having count(*) > 50;
</code></li>
<li><code>select store_id, count(*) from customer
group by store_id;
</code></li>
<li><code>select country_id, count(*) from city
group by country_id 
order by count desc
limit 1;
</code></li>
 </ol>
