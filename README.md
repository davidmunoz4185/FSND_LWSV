# Linux Web Server in Full Stack Nanodegree ...

### Let me access ...

##### IP Address and SSH Port

* IP: 34.200.97.254
* Port: 2200

### Let me see your application ...

You can access by the following link:

http://34.200.97.254

### Let me know which software ...

In requirements.txt you can see ALL!!!

### Let me know what else ...

Ok, you are right, perhaps I forgot to mention:

* apache2
* postgresql
* mod_wsgi

### Let me know how you did it ...

Ok first I installed apache2 & mod_wsgi:

`sudo apt-get install apache2 libapache2-mod-wsgi`

and verified that it worked by:

http://34.200.97.254

Once this task is done:

`sudo vi /etc/apache2/sites-enabled/000-default.conf`

with the following content:

```javascript

<VirtualHost *:80>
        WSGIScriptAlias / /home/grader/catalog/application.wsgi
        ErrorLog /var/www/logs/error.log
        CustomLog /var/www/logs/access.log combined

        <Directory /home/grader/catalog>
                Require all granted
        </Directory>
</VirtualHost>
```
and downloaded git Repository in /home/grader/catalog

After that I created /home/grader/catalog/application.wsgi file

```
vi /home/grader/catalog/application.wsgi

import sys

sys.path.insert(0, '/home/grader/catalog')

from application import app as application

```

### And finally ...

I hope you like it!!!

