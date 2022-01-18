### Aşağıdaki sorgu senaryolarını dvdrental örnek veri tabanı üzerinden gerçekleştiriniz.

<ol>
<li>city tablosu ile country tablosunda bulunan şehir (city) ve ülke (country) isimlerini birlikte görebileceğimiz LEFT JOIN sorgusunu yazınız.
 </li>
<li>customer tablosu ile payment tablosunda bulunan payment_id ile customer tablosundaki first_name ve last_name isimlerini birlikte görebileceğimiz RIGHT JOIN sorgusunu yazınız.
 </li>
<li>customer tablosu ile rental tablosunda bulunan rental_id ile customer tablosundaki first_name ve last_name isimlerini birlikte görebileceğimiz FULL JOIN sorgusunu yazınız.
 </li>
 </ol>

### Çözüm:

<ol>
<li><code>SELECT city.city, country.country FROM city
LEFT JOIN country ON city.country_id = country.country_id;
</code></li>
<li><code>SELECT payment_id, first_name, last_name FROM customer
RIGHT JOIN payment ON customer.customer_id = payment.customer_id;
</code></li>
<li><code>SELECT rental_id, first_name, last_name FROM customer
FULL JOIN rental ON customer.customer_id = rental.customer_id;
</code></li>
 </ol>
