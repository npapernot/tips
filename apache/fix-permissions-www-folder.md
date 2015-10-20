# Fix Permissions on WWW folder
Sometimes apache2 has permissions issues with `/var/www/html/`. To fix
ownership and access permissions (to allow access from browsers pointing to
http://localhost), run the following chmod and chown:  

`sudo chmod 777 /var/www/ -R`
`sudo chown www-data:www-data /var/www/ -R` 
