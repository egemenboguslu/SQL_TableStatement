* Tablo oluşturmak için;
```
CREATE TABLE author(
	id SERIAL PRIMARY KEY,
	first_name VARCHAR(50) NOT NULL,
	last_name VARCHAR(50) NOT NULL,
	email VARCHAR(50),
	birthday DATE
);
```
* Tabloya eleman eklemek için;
```
INSERT INTO author(first_name,last_name,email,birthday)
VALUES
    ('Sabahattin','Ali','sabahattin@ali.com','1907/02/25');
```
* Var olan tabloya benzer yeni tablo oluşturmak için;
```
CREATE TABLE author2 (LIKE author);
```
* Var olan tablonun verileri ile beraber yeni tablo oluşturmak için;
```
CREATE TABLE author3 AS
SELECT* FROM author; 
```
* Yeni tabloya ilk tablodan veri kopyalama;
```
INSERT INTO author2
SELECT * FROM author
WHERE first_name = 'Sabahattin';
```
* Tablo silmek için;
```
DROP TABLE author3;
```
* ID = 10 olan yazarı yeni yazar ile update etme;
```
UPDATE author
SET 
	first_name = 'XXX',
	last_name = 'YYY',
	email = 'xxx@yyy.com'
WHERE id = 10;
```
* Sadece değişiklik yapılan satırı görmek için;
```
UPDATE author
SET 
	first_name = 'XXX',
	last_name = 'YYY',
	email = 'xxx@yyy.com'
WHERE id = 10
RETURNING *; 
```
* ilk isminin baş harfi 'K' olan tüm yazarları güncelleme;
```
UPDATE author
SET
	first_name = 'UPDATE'
WHERE first_name LIKE 'K%';
```
* id no'su 10dan büyük verileri silip görmek için;
```
DELETE FROM author
WHERE id > 11
RETURNING *;
```



















