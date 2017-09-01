#03_webserver

架設網頁伺服器

***

安裝apache2,php,mariadb

`sudo apt-get install apache2 php php-mysql mysql-server`

![amp](img/01.png)

安裝確認

![安裝確認](img/02.png)

開啟瀏覽器在網址列輸入localhost或者IP

![web](img/03.png)

***

進入資料庫並修改密碼

`sudo mysql -u root -p`

![sql](img/04.png)

選擇mysql資料庫

`use mysql;`

![mysql](img/05.png)

修改root密碼

`UPDATE user SET Password=PASSWORD('pswd') where USER='root';`

![pswd](img/06.png)

修改資料庫權限

`GRANT all ON *.* TO root@'localhost' IDENTIFIED BY 'pswd';`

![db](img/07.png)

刷新緩衝區

`FLUSH PRIVILEGES;`

![FLUSH](img/08.png)
