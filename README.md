Twenty_Thirteen_clean
=====================

A clean wordpress template, based on Twenty_Thirteen + grunt.


Good practice and cool plugin to install :
-----
- install WP Smush.it (to install before adding images to posts)
- install W3 Total Cache (to activate once the development is over or you will not be able to see your css and js updates)
- install WP-Optimize (db cleaner)
- in wp-config.php add `define('WP_POST_REVISIONS',2);` to keep only 2 revisions max per posts
- in .htaccess add :
```
<FilesMatch "\.(ico|pdf|flv|jpg|jpeg|png|gif|js|css|swf)(\.gz)?$">
Header set Expires "Thu, 15 Apr 2016 20:00:00 GMT"
Header unset ETag
FileETag None
</FilesMatch>

# Content expiration headers
<IfModule mod_expires.c>
    ExpiresActive On

    ExpiresDefault "access"

    ExpiresByType text/html "access"
    ExpiresByType text/xml "access"
    ExpiresByType application/xml "access"
    ExpiresByType application/xhtml+xml "access"
    ExpiresByType text/css "access plus 1 month"
    ExpiresByType text/javascript "access plus 1 month"
    ExpiresByType text/x-javascript "access plus 1 month"
    ExpiresByType application/javascript "access plus 1 month"
    ExpiresByType application/x-javascript "access plus 1 month"
    ExpiresByType image/gif "access plus 1 month"
    ExpiresByType image/jpg "access plus 1 month"
    ExpiresByType image/jpeg "access plus 1 month"
    ExpiresByType image/png "access plus 1 month"
    ExpiresByType application/pdf "access plus 1 month"
    ExpiresByType application/x-shockwave-flash "access plus 1 month"
    ExpiresByType image/ico "access plus 1 year"
    ExpiresByType image/icon "access plus 1 year"
    ExpiresByType image/x-icon "access plus 1 year"

    # Need to register the icon mime type
    AddType image/vnd.microsoft.icon .ico
    ExpiresByType image/vnd.microsoft.icon "access plus 1 year"

    # Add correct content-type for fonts
    AddType application/vnd.ms-fontobject .eot
    AddType application/x-font-ttf .ttf
    AddType application/x-font-opentype .otf
    AddType application/x-font-woff .woff
    AddType image/svg+xml .svg

    # Compress compressible fonts
    AddOutputFilterByType DEFLATE application/x-font-ttf application/x-font-opentype image/svg+xml

    # Add a far future Expires header for fonts
    ExpiresByType application/vnd.ms-fontobject "access plus 1 year"
    ExpiresByType application/x-font-ttf "access plus 1 year"
    ExpiresByType application/x-font-opentype "access plus 1 year"
    ExpiresByType application/x-font-woff "access plus 1 year"
    ExpiresByType image/svg+xml "access plus 1 year"

</IfModule>
```
