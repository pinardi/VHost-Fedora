Virtual Hosting Fedora
# Install http
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
   ServerName www.srv.world
</VirtualHost>

# for virtual domain
<VirtualHost *:80>
   DocumentRoot /var/www/html
   ServerName www.virtual.host
   ServerAdmin webmaster@virtual.host
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
Virtual Host Test Page
</div>
</body>
</html>
```
open browser and type www.virtual.host
