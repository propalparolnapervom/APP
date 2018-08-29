# APACHE HTTP MAINTENANCE (LINUX)



## USEFULL LINKS

[Getting Started](https://httpd.apache.org/docs/trunk/getting-started.html)



## MAINTENANCE

### VERSION

Check version installed
```
httpd -v

      Server version: Apache/2.2.34 (Unix)
      Server built:   Nov  1 2017 18:47:16
```

### START/STOP/STATUS

**Check status**
```
service httpd status
```

**Start**
```
/sbin/service httpd start
```

**Stop**
```
/sbin/service httpd stop
```

**Re-start**
```
 /sbin/service httpd restart
```



### CONFIG FILES AND DIRECTIVES

[Default File Places](https://wiki.apache.org/httpd/DistrosDefaultLayout)

```
#Fedora Core, CentOS, RHEL:

ServerRoot              ::      /etc/httpd
Primary Config Fle      ::      /etc/httpd/conf/httpd.conf
Other Config Files      ::      /etc/httpd/conf.d
Module Locations        ::      /usr/lib/httpd/modules
DocumentRoot            ::      /var/www/html
ErrorLog                ::      /var/log/httpd/error_log
AccessLog               ::      /var/log/httpd/access_log
cgi-bin                 ::      /var/www/cgi-bin (empty and disabled by default)
binary                  ::      /usr/sbin/httpd
runtime directory       ::      /etc/httpd/run
start/stop              ::      /sbin/service httpd {start|stop|restart|condrestart|reload|status|fullstatus|graceful|help|configtest}
```

**Notes**:
  - There is an extra config file in `/etc/sysconfig/httpd` which can be used to change to the worker mpm `/usr/sbin/httpd.worker`.
  - Extra config files named `*.conf` are loaded from `/etc/httpd/conf.d`. This dir is used by packages like `mod_python` for drop-in configs
  - If you're having issues with authorization and your permissions are correct, you might have problems with SELinux permissions. Take a look at [httpd_selinux(8)](http://people.fedoraproject.org/~dwalsh/SELinux/httpd_selinux.html) and related documentation. Particularly sealert(8) can be used for analysis and suggested solutions.

























