Virtual Hosting Fedora
# Install httpd
```bash
yum install http
```
# Open vhost config
```bash
nano /etc/httpd/conf.d/vhost.conf
```
# create new Config VHost
```bash
# for original domain
<VirtualHost *:80>
   DocumentRoot /var/www/html
   ServerName www.jweb.com
</VirtualHost>

# for virtual domain
<VirtualHost *:80>
   DocumentRoot /var/www/html
   ServerName www.jweb.com
   ServerAdmin webmaster@jweb.com
</VirtualHost>
```
# systemctl restart httpd 
# create new file index.html
```bash
nano /var/www/html 
```
```bash
 <html>
<body>
<div style="width: 100%; font-size: 40px; font-weight: bold; text-align: center;">
         JWEB Test Page
</div>
</body>
</html>
```
open browser and type www.jweb.com
