# djangostockapplication
TR 

Django Stock App Projesi Açıklaması Bu Django projesi, bir stok yönetim ve satış takip uygulamasını gerçekleştirmeyi amaçlamaktadır. 

Proje, aşağıdaki ana modelleri içerir: Category, Brand, Product, Firm, Purchases, Sales ve User. Bu modeller arasında çeşitli ilişkiler kurularak, stok takibi ve satış yönetimi sağlanmaktadır.

1- Category Tablosu:

name:

2- Brand Tablosu:

name:

image:

3- Product Tablosu:

name:

category: Category Tablosu ile uygun olan ilişki kurulmalıdır. ForeigneKey - OneToOne veya ManyToMany

brand: Brand Tablosu ile uygun olan ilişki kurulmalıdır. ForeigneKey - OneToOne veya ManyToMany

stock:

created:

updated:

4- Firm Tablosu:

name:

phone:

address:

image:

created:

updated:

5- Purchases Tablosu:
user: UserTablosu ile uygun olan ilişki kurulmalıdır. ForeigneKey - OneToOne veya ManyToMany

firm: Firm Tablosu ile uygun olan ilişki kurulmalıdır. ForeigneKey - OneToOne veya ManyToMany

brand: Brand Tablosu ile uygun olan ilişki kurulmalıdır. ForeigneKey - OneToOne veya ManyToMany

quantity:

price:

price_total:

created:

updated:

6- Sales Tablosu:

user: UserTablosu ile uygun olan ilişki kurulmalıdır. ForeigneKey - OneToOne veya ManyToMany

product: Product Tablosu ile uygun olan ilişki kurulmalıdır. ForeigneKey - OneToOne veya ManyToMany

brand: Brand Tablosu ile uygun olan ilişki kurulmalıdır. ForeigneKey - OneToOne veya ManyToMany

quantity:

price:

price_total:

created:

updated:

7- Bir Category’e ait toplam ürün sayısını hesaplayan method yazılmalı

8-  Category search(name) ve filter(name) özellikleri eklenmeli

9- Category’e giriş noktasındaki name filtresini kullanarak arama yaparken Category’e ait ürün(products)  ayrıntılarını görüntülemek için yeni bir serializer oluşturulmalı.

10- Category’e siteye login olan her kullanıcı CRUD işlemi yapabilsin olmayanlar sadece GET isteğinde response alabilsin.

11-  Brand search(name) özellikleri eklenmeli

12- Brand’e siteye login olan her kullanıcı CRUD işlemi yapabilsin olmayanlar sadece GET isteğinde response alabilsin.

13-  Firm search(name) özellikleri eklenmeli

14- Firm’e siteye login olan her kullanıcı CRUD işlemi yapabilsin olmayanlar sadece GET isteğinde response alabilsin.

15-  Product search(name) ve filter(category, brand) özellikleri eklenmeli

16- Product’e siteye login olan her kullanıcı CRUD işlemi yapabilsin olmayanlar sadece GET isteğinde response alabilsin.

17- Product Toblosundaki stock field’ı sales ve purchases bilgilerine göre azalma ve artmaya yaşaması gerekiyor bu sebepten kaynaklı stock field’ı read_only olmalı

18- Purchases Tablosunda price_total field’ını hesaplatmanız gerekmektedir. price field’ı 1 adet ürünün fiyatı iken satın alınan ürün adedi ile ürün fiyatının matemetiksel bir hesaplama sonucu bir değer alması gerekmektedir.

19-  Purchases search(firm) ve filter(firm, product) özellikleri eklenmeli

20- Purchases ’e siteye login olan her kullanıcı CRUD işlemi yapabilsin olmayanlar sadece GET isteğinde response alabilsin.

21- Purchases yani ibr ürün satın alındığında satın alınan ürünün product tablosundaki stock miktarının artması gerekmektedir.

22- user tabblosu ile ilişki kurulan her tabloda isteği atan kişinin otomatik olarak user bilgileri alınması gerekmektedir.

23- Purchases update edilme durumda da stock miktarları hesaba katılmalı

24- Purchases delete edilmesi durumda da stock miktarı düşürülmeli

25- Purcheses’a eklenen ürünlerin category bilgileride purcaheses datasının içine eklenmeli

26- Purchases’da yaptığımız şeyleri Sales içinde benzerini yapıcaz herhangi bir product tablosundaki ürün satılırsa Sales miktarı product stock miktarından düşülmeli ve stock sayından daha fazla bir sales olursa izin vermeden uyarı vermeli

27-  Sales search(brand) ve filter(brand, product) özellikleri eklenmeli

28- Sales’e siteye login olan her kullanıcı CRUD işlemi yapabilsin olmayanlar sadece GET isteğinde response alabilsin.
