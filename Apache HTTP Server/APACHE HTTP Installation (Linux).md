# APACHE HTTP INSTALLATION (Linux)


**1. INSTALL APACHE**

Install Apache software
```
yum install -y httpd
```

Start Apache
```
service httpd start
```

Make sure it starts every time automatically
```
chkconfig httpd on
```

**2. VERIFY INSTALLATION WITH TEST HTML**

Create simple test html-page
```
cd /var/www/html
touch index.html
vi index.html
  
  <html><h1> XBURSER: Test is successfull!!! </h1></html>
```

Verify its availability
```
http://52.59.237.102
```




































