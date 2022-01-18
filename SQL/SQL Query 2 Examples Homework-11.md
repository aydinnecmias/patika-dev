### Aşağıdaki sorgu senaryolarını dvdrental örnek veri tabanı üzerinden gerçekleştiriniz.

<ol>
<li>actor ve customer tablolarında bulunan first_name sütunları için tüm verileri sıralayalım.
 </li>
<li>actor ve customer tablolarında bulunan first_name sütunları için kesişen verileri sıralayalım.
 </li>
<li>actor ve customer tablolarında bulunan first_name sütunları için ilk tabloda bulunan ancak ikinci tabloda bulunmayan verileri sıralayalım.
 </li>
<li>İlk 3 sorguyu tekrar eden veriler için de yapalım.
 </li>
 </ol>

### Çözüm:

<ol>
<li><code>SELECT first_name FROM actor
UNION
SELECT first_name FROM customer;
</code></li>
<li><code>SELECT first_name FROM actor
INTERSECT
SELECT first_name FROM customer;
</code></li>
<li><code>SELECT first_name FROM actor
EXCEPT
SELECT first_name FROM customer;
</code></li>
<li><code>SELECT first_name FROM actor UNION ALL SELECT first_name FROM customer;<br>
SELECT first_name FROM actor EXCEPT ALL SELECT first_name FROM customer;<br>
--INTERSECT ALL VE INSTERSECT AYNI SONUCU VERİR.
</code></li>
 </ol>
