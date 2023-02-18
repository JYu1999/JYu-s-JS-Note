1. 建議對 laravel 有一定認識，手上有做好一個簡單專案再來嘗試
2. 先了解 hosting 是什麼，有哪些種類
   - [不是工程師 架站用VPS還是Web Hosting，中文翻譯都有「虛擬」到底差在哪？](https://progressbar.tw/posts/102)
   - [學習VPS的重要性與各大Linux VPS 比較與推薦 (Linode, DigitalOcean, Vultr, AWS Lightsail)
](https://progressbar.tw/posts/131)
2. 想辦法開一個 VPS 或 Cloud Host，然後 ssh 進去
3. 安裝 LEMP
   - [How To Install Linux, Nginx, MySQL, PHP (LEMP stack) on Ubuntu 22.04](https://www.digitalocean.com/community/tutorials/how-to-install-linux-nginx-mysql-php-lemp-stack-on-ubuntu-22-04)
   - [How To Install LEMP Stack On Ubuntu 22.04](https://cloudcone.com/docs/article/how-to-install-lemp-stack-on-ubuntu-22-04/)
   - 安裝過程中，務必注意啟用 ufw 之後，要把 ssh 開起來，否則會出現 server 還活著，但就是 ssh 不進去的狀況。
     - [Ufw Firewall Allow SSH](https://linuxhint.com/ufw-firewall-allow-ssh/)
 - [How To Install MariaDB on Ubuntu 22.04](https://www.digitalocean.com/community/tutorials/how-to-install-mariadb-on-ubuntu-22-04)
4. serve複數個網站
   - [How to Host Multiple Websites on One Server](https://www.cloudpanel.io/tutorial/how-to-host-multiple-websites-on-one-server/#steps-to-host-multiple-websites-on-one-server--nginx)
   - [How to Configure Nginx to serve Multiple Websites on a Single VPS](https://webdock.io/en/docs/how-guides/shared-hosting-multiple-websites/how-configure-nginx-to-serve-multiple-websites-single-vps)
5. Install and deploy Multiple Laravel Projects
   - [How to Install and Configure Laravel 8 with Nginx (LEMP) on Ubuntu 18.04](https://www.digitalocean.com/community/tutorials/how-to-install-and-configure-laravel-with-lemp-on-ubuntu-18-04)
   - [How to Deploy A Laravel App With Nginx on Ubuntu(LEMP)](https://www.iankumu.com/blog/how-to-deploy-a-laravel-app-on-lemp-stack/)
6. 可以往 [API Learning Path](obsidian://open?vault=JYu's%20Obsidian&file=pages%2FAPI%20Learning%20Path) 前進