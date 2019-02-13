# docker-haproxy-nginx

## Usage

```sh
$ docker-compose up
```

haproxy needs the cert and key to be combined. These are copied to the container by the compose file.

```sh
$ openssl req -subj '/CN=localhost' -x509 -newkey rsa:4096 -nodes -keyout key.pem -out cert.pem -days 365
$ cat cert.pem key.pem > cert.key.pem
```

This is for HTTPS termination

https://stuff-things.net/2016/11/30/haproxy-sni/ not used here

https://medium.com/@oliver.zampieri/self-signed-ssl-reverse-proxy-with-docker-dbfc78c05b41
