CodeigniterRemoveIndex
======================

Codeigniter remove index.php file from url

Put .htaccess file out side from application folder and following code put that file and save it.

<IfModule mod_rewrite.c>

    Options +FollowSymLinks
    RewriteEngine on

    # Send request via index.php
    RewriteCond %{REQUEST_FILENAME} !-f
    RewriteCond %{REQUEST_FILENAME} !-d
    RewriteRule ^(.*)$ index.php/$1 [L]

</IfModule>

After in config.php file set $config['index_page'] = '';
