openssl genrsa -out site.key 2048

openssl req -new -key site.key -out site.net.csr
cp old_certs/site.net.ext .

openssl x509 -req -in site.csr -CA CA.pem -CAkey CA.key -CAcreateserial -out site.crt -days 30 -sha256 -extfile site.ext
