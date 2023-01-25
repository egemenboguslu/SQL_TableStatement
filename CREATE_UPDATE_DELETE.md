1) test veritabanınızda employee isimli sütun bilgileri id(INTEGER), name VARCHAR(50), birthday DATE, email VARCHAR(100) olan bir tablo oluşturalım.
```
CREATE TABLE employee(
  
	id INTEGER,
	name VARCHAR(50),
	birthday DATE,
	email VARCHAR(100)
  
);
```
2) Oluşturduğumuz employee tablosuna 'Mockaroo' servisini kullanarak 50 adet veri ekleyelim.

	#### Mockaroo
	-----
	[Click Here!](https://www.mockaroo.com)

3) Sütunların her birine göre diğer sütunları güncelleyecek 1 adet UPDATE işlemi yapalım.
```
UPDATE employee
SET name = 'XXX YYY',
    birthday = '1996-03-13',
    email = 'abc@def.com'
WHERE id =1;
```
4) Sütunların her birine göre ilgili satırı silecek 1 adet DELETE işlemi yapalım.
```
DELETE FROM employee
WHERE name LIKE 'V%';
```

