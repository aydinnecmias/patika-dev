### Test Veritabanı işlemleri

<ol>
<li>Test veritabanınızda employee isimli sütun bilgileri id(INTEGER), name VARCHAR(50), birthday DATE, email VARCHAR(100) olan bir tablo oluşturalım.
 </li>
<li>Oluşturduğumuz employee tablosuna 'Mockaroo' servisini kullanarak 50 adet veri ekleyelim.
 </li>
<li>Sütunların her birine göre diğer sütunları güncelleyecek 5 adet UPDATE işlemi yapalım.
<li>Sütunların her birine göre ilgili satırı silecek 5 adet DELETE işlemi yapalım.
 </li>
 </ol>

### Çözüm:

<li>3-UPDATE <br>
<code>UPDATE employee
SET first_name = 'aydin '
WHERE id = 1
RETURNING *;<br>
UPDATE employee
SET id = 1903
WHERE id = 4
RETURNING *;<br>
UPDATE employee
SET last_name = 'as'
WHERE id = 1;<br>
UPDATE employee
SET email = 'aydin@gmail.com'
WHERE id = 1;<br>
UPDATE employee
SET birthday = '2022-01-01'
WHERE id = 1;<br>
</code></li>
<li>4-DELETE <br>
<code>DELETE FROM employee
WHERE id = 1;<br>
DELETE FROM employee
WHERE first_name ='necmi';<br>
DELETE FROM employee
WHERE email ='ftyzack5@imageshack.us';<br>
DELETE FROM employee
WHERE birthday ='2021-01-09';<br>
DELETE FROM employee
WHERE id ='1903';
</code></li>
