# nginx-alpine-ssl

For using a self-signed cert on a (fake) custom domain to run on `localhost`.

Copied code from https://medium.com/@codingwithmanny/configure-self-signed-ssl-for-nginx-docker-from-a-scratch-7c2bcd5478c6

Steps to run:
```
docker run -it -d -p 80:80 -p 443:443 --name test nginxssltest

curl localhost;
# Expected output
# <h1>Hello world!</h1>

curl https://localhost --insecure;
# Expected output
# <h1>Hello world!</h1>
```
