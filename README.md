# smarthome-docker-compose
An nginx reverse proxy for homeassistant and duck dns.  
Based off my [foundry-vtt configuration](https://github.com/jeottesen/foundry-docker-compose). But since that 
was running on an AWS server I didn't need to set up DuckDNS. DuckDNS will let me host homeassistant from my home network.

Files to change before it will work. Change "my_server: to your domain name  
files:  
[.env](.env) Line 1  
[containers/nginx/config/conf.d/default.conf](containers/nginx/config/conf.d/default.conf) Line 2, 12  
[containers/nginx/config/conf.d/homeassistant.conf](containers/nginx/config/conf.d/foundry.conf) Line 2, 7  
  
  
Add your email to this file.  
[init-letsencrypt.sh](init-letsencrypt.sh) Line 12  
  
[init-letsencrypt.sh](init-letsencrypt.sh) script originally from here.  
[https://github.com/wmnnd/nginx-certbot/blob/master/init-letsencrypt.sh](https://github.com/wmnnd/nginx-certbot/blob/master/init-letsencrypt.sh)