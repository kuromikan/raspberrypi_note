#02_locale

語言設定為繁體中文及新增輸入法

***

安裝中文桌面

`sudo aptitude -y install task-chinese-t-desktop`

![中文桌面](img/01.png)

修改鍵盤設定

`sudo nano /etc/default/keyboard`

![修改鍵盤設定](img/02.png)

XKBLAYOUT="us"

![鍵盤設定](img/03.png)

使用Ctrl+O存檔之後Ctrl+X離開後重新開機

***

進入樹莓派設定

`sudo raspi-config`

![raspi-config](img/04.png)

選擇4語言設定

![localisation options](img/05.png)

選擇1語言設定

![change locale](img/06.png)

選擇zh_TW.BIG5,zh_TW.EUC-TW EUC-TW,zh_TW.UTF-8 UTF-8

![configuring locales](img/07.png)

將環境選擇 zh_TW.UTF-8

![configuring locales](img/08.png)

設定時區

![change timezone](img/09.png)

選擇Asia

![configuring tzdata](img/10.png)

選擇Taipei

![configuring tzdata](img/11.png)

完成

![raspi-config](img/12.png)

重新開機後環境變成繁體中文

![desktop](img/13.png)

***

安裝輸入法

`sudo apt-get install scim scim-tables-zh scim-chewing scim-gtk-immodule im-switch`

![scim](img/14.png)

![scim](img/15.png)

Ctrl+Space切換輸入法

![scim](img/16.png)