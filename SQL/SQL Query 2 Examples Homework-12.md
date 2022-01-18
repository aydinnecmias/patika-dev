### Aşağıdaki sorgu senaryolarını dvdrental örnek veri tabanı üzerinden gerçekleştiriniz.

<ol>
<li>film tablosunda film uzunluğu length sütununda gösterilmektedir. Uzunluğu ortalama film uzunluğundan fazla kaç tane film vardır?
 </li>
<li>film tablosunda en yüksek rental_rate değerine sahip kaç tane film vardır?
 </li>
<li>film tablosunda en düşük rental_rate ve en düşük replacement_cost değerlerine sahip filmleri sıralayınız.
<li>payment tablosunda en fazla sayıda alışveriş yapan müşterileri(customer) sıralayınız.
 </li>
 </ol>

### Çözüm:

<ol>
<li><code>SELECT COUNT(*) length FROM film  WHERE length >
(
	SELECT AVG(length) FROM film 
);
</code></li>
<li><code>SELECT COUNT(*) FROM film 
WHERE length = (SELECT MAX(length) FROM film);
</code></li>
<li><code>SELECT title, replacement_cost, rental_rate FROM film
WHERE rental_rate = (SELECT MIN(rental_rate) FROM film) 
AND
replacement_cost =(SELECT MIN(replacement_cost) FROM film);
</code></li>
<li><code>SELECT first_name,last_name,
(
	SELECT COUNT(*) FROM payment  WHERE payment.customer_id = customer.customer_id
) as payment  FROM customer	
ORDER BY payment DESC
LIMIT 1;

</code></li>

 </ol>
