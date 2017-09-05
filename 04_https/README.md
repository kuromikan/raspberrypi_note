#04_https

如何建立憑證及在網頁伺服器上載入

***

建立資料夾

`sudo mkdir /etc/apache2/ssl`

![mkdir](img/01.png)

建立crt及key

`sudo openssl req -x509 -nodes -days 3650 -newkey rsa:2048 -out /etc/apache2/ssl/server.crt -keyout /etc/apache2/ssl/server.key`

![crt_key](img/02.png)

建立憑證時所需輸入的資訊

![key](img/03.png)

啟用ssl模組

`sudo a2enmod ssl`

![ssl](img/04.png)

連結sites-available/default-ssl.conf到sites-enabled/000-default-ssl.conf

`sudo ln -s /etc/apache2/sites-available/default-ssl.conf /etc/apache2/sites-enabled/000-default-ssl.conf`

![ssl.conf](img/05.png)

編輯sites-enabled/000-default-ssl.conf

`sudo nano /etc/apache2/sites-enabled/000-default-ssl.conf`

![ssl.conf](img/06.png)

使用ctrl+w搜尋到要修改的位置，將剛才建立好的crt及key填上

![ssl.conf](img/07.png)

重新啟動apache

`sudo /etc/init.d/apache2 restart`

![restart](img/08.png)

開啟瀏覽器在網址列輸入https://localhost

![web](img/09.png)

跳出安全性確認

![web](img/10.png)

瀏覽網頁

![web](img/11.png)