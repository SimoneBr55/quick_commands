```
openssl s_client -starttls smtp -showcerts -connect mail.yourdomain.com:25 -servername mail.yourdomain.com  # to verify that the certificate has expired.
postmap -F hash:/etc/postfix/vmail_ssl.map
systemctl restart dovecot.service
systemctl restart postfix
openssl s_client -starttls smtp -showcerts -connect mail.yourdomain.com:25 -servername mail.yourdomain.com  # check again
```
