# Steps

Note: Replace any mention of `nginx.evermight.net` with your fully qualified domain name.

1. Run `apt-get install -y nginx snapd` to download tools you will need;
2. Copy the file `etc/nginx/sites-available/nginx.evermight.net` to `/etc/nginx/sites-available/nginx.evermight.net`.
3. Edit `/etc/nginx/sites-available/nginx.evermight.net` with the relevant port forwarding values.
4. Run `ln -s /etc/nginx/sites-available/nginx.evermight.net /etc/nginx/sites-enabled/nginx.evermight.net`.
5. Run `systemctl restart nginx`.
6. Install TLS certs with certbot:

```
snap install certbot --classic;
certbot --nginx -d nginx.evermight.net
```
