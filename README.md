# djangostockapplication

ENG 

Description of Django Stock App Project

This Django project aims to implement an inventory management and sales tracking application.

The project includes the following main models: Category, Brand, Product, Firm, Purchases, Sales, and User.

Various relationships are established between these models to provide inventory tracking and sales management.

1.Category Table:

name:

2.Brand Table:

name:

image:

3.Product Table:

name:

category: Should establish a relationship with the Category Table. ForeignKey - OneToOne or ManyToMany.

brand: Should establish a relationship with the Brand Table. ForeignKey - OneToOne or ManyToMany.

stock:

created:

updated:

4.Firm Table:

name:

phone:

address:

image:

created:

updated:

5.Purchases Table:

user: Should establish a relationship with the User Table. ForeignKey - OneToOne or ManyToMany.

firm: Should establish a relationship with the Firm Table. ForeignKey - OneToOne or ManyToMany.

brand: Should establish a relationship with the Brand Table. ForeignKey - OneToOne or ManyToMany.

quantity:

price:

price_total:

created:

updated:

6.Sales Table:

user: Should establish a relationship with the User Table. ForeignKey - OneToOne or ManyToMany.

product: Should establish a relationship with the Product Table. ForeignKey - OneToOne or ManyToMany.

brand: Should establish a relationship with the Brand Table. ForeignKey - OneToOne or ManyToMany.

quantity:

price:

price_total:

created:

updated:

7.A method should be written to calculate the total number of products for a Category.

8.Add search(name) and filter(name) features for Category.

9.Create a new serializer to view the details of products belonging to a Category when searching using the name filter at the Category entry point.

10.Allow CRUD operations for users logged into the site for Category; only allow GET requests for non-logged-in users.

11.Add search(name) feature for Brand.

12.Allow CRUD operations for users logged into the site for Brand; only allow GET requests for non-logged-in users.

13.Add search(name) feature for Firm.

14.Allow CRUD operations for users logged into the site for Firm; only allow GET requests for non-logged-in users.

15.Add search(name) and filter(category, brand) features for Product.

16.Allow CRUD operations for users logged into the site for Product; only allow GET requests for non-logged-in users.

17.The stock field in the Product Table should be read-only, as it should decrease or increase based on sales and purchases information.

18.Calculate the price_total field in the Purchases Table. The price field represents the price of one unit, and the price_total should be the result of a mathematical calculation based on the quantity.

19.Add search(firm) and filter(firm, product) features for Purchases.

20.Allow CRUD operations for users logged into the site for Purchases; only allow GET requests for non-logged-in users.

21.When a product is purchased, the stock quantity in the Product Table should increase.

22.Automatically retrieve user information for each table where a relationship is established with the user table.

23.When updating Purchases, consider stock quantities.

24.When deleting Purchases, decrease the stock quantity.

25.Include category information for products added to Purchases in the Purchases data.

26.Similar operations performed in Purchases should be implemented in Sales. If a product in the Product Table is sold, the Sales quantity should be subtracted from the product stock quantity. If the sales exceed the stock quantity, issue a warning without allowing it.

27.Add search(brand) and filter(brand, product) features for Sales.

28.Allow CRUD operations for users logged into the site for Sales; only allow GET requests for non-logged-in users.

TR 

Django Stock App Projesi Açıklaması Bu Django projesi, bir stok yönetim ve satış takip uygulamasını gerçekleştirmeyi amaçlamaktadır. 

Proje, aşağıdaki ana modelleri içerir: Category, Brand, Product, Firm, Purchases, Sales ve User.

Bu modeller arasında çeşitli ilişkiler kurularak, stok takibi ve satış yönetimi sağlanmaktadır.

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
