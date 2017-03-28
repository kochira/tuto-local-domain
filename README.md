Ajouter un nouveau virtual host avec MAMP!
===================


Editez le fichier host de votre mac
-------------

Prenez garde à bien ouvrir le fichier en super admin
```
sudo vim /private/etc/hosts
```

Exemple de vhost : 
```
127.0.0.1       domain.local
```

Editez le vhost Mamp
------------
Ouvrez le fichier httpd-vhosts.conf avec votre éditeur (vim, nano)

```
vim /Applications/MAMP/conf/apache/extra/httpd-vhosts.conf
```

Puis, ajoutez une entrée supplémentaire comme dans l'exemple suivant :

```
<VirtualHost *:80>
    ServerAdmin user@your-domain.net
    DocumentRoot "/Applications/MAMP/htdocs/project_root"
    ServerName domain.local
</VirtualHost>
```

> **Pour finir, pensez a redémarrer votre serveur Apache.**
