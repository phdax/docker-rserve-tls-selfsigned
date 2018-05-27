docker-rserve-tls-selfsigned
=============

Rserve with TLS/SSL connection mode by self-signed certificate

## Run
### simply
```
docker run -d -p 6313:6313 phdax/docker-rserve-tls-selfsigned
```
### persist library and workspace
```
docker run -d -p 6313:6313 \
-v [LOCAL LIB DIR]:/opt/r/lib \
-v [LOCAL WORK DIR]:/opt/r/work \
phdax/docker-rserve
```

## Usage
### connection
user : admin \
pass : admin \
port : 6313
### get server crt/pem
```
docker copy [CONTAINER TAG]:/opt/r/Rserve.crt .
docker copy [CONTAINER TAG]:/opt/r/Rserve.pem .
```