# APACHE HTTP INSTALLATION (Linux)


**1. Install Apache**

Install Apache software
```
yum install -y httpd
```

Start Apache
```
service httpd start
```


**2. Place necessary html**
```
cd /var/www/html
touch index.html
vi index.html
  
  <html><h1> XBURSER: Test is successfull!!! </h1></html>
```

**3. Check web-page availability**
```
http://52.59.237.102
```




































