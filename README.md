# nginx-docker-compose
An extendable nginx reverse proxy.  
Usefull for homeassistant, plex, foundryvtt, and more.

Easily add subdomain proxies and subpath proxies. Get ssl up and running through letsencrpyt and certbot.

Run init-letsencrypt.sh after setting up docker and docker-compose. Set the staging to two and configure the email and domains to test. When setup is complete and nginx is accessible from the domain set staging to 0 and run it again to build the real certificate.
  
Files to change before it will work. Change "my_server: to your domain name  
files:  
[.env](.env) Line 1  
[scripts/init-letsencrypt.sh](scripts/init-letsencrypt.sh) Line 11  
[containers/nginx/config/conf.d/default.conf](containers/nginx/config/conf.d/default.conf) Line 2, 12  
[containers/nginx/config/conf.d/homeassistant.conf](containers/nginx/config/conf.d/foundry.conf) Line 2, 7  
[containers/nginx/config/ssl.conf](containers/nginx/config/ssl.conf) Line 1, 2  
  
  
Add your email to this file.  
[scripts/init-letsencrypt.sh](scripts/init-letsencrypt.sh) Line 12  
  
[scripts/init-letsencrypt.sh](scripts/init-letsencrypt.sh) script originally from here.  
[https://github.com/wmnnd/nginx-certbot/blob/master/init-letsencrypt.sh](https://github.com/wmnnd/nginx-certbot/blob/master/init-letsencrypt.sh)