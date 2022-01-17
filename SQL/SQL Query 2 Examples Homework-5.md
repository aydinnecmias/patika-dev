### Aşağıdaki sorgu senaryolarını dvdrental örnek veri tabanı üzerinden gerçekleştiriniz.

<ol>
<li>film tablosunda bulunan ve film ismi (title) 'n' karakteri ile biten en uzun (length) 5 filmi sıralayınız.
 </li>
<li>film tablosunda bulunan ve film ismi (title) 'n' karakteri ile biten en kısa (length) ikinci(6,7,8,9,10) 5 filmi(6,7,8,9,10) sıralayınız.
 </li>
<li>customer tablosunda bulunan last_name sütununa göre azalan yapılan sıralamada store_id 1 olmak koşuluyla ilk 4 veriyi sıralayınız.
 </li>
 </ol>

### Çözüm:

<ol>
<li><code>select * from film where title like '%n' order by length desc
limit 5 ;
</code></li>
<li><code>select * from film where title like '%n'
order by  length
offset 5
limit 5 ;
</code></li>
<li><code>select * from customer
where store_id = 1
order by last_name desc
limit 4;
</code></li>
 </ol>
