server {
    listen 80;
    server_name localhost;

    location / {
        root /var/www/html;
        index index.html;
        try_files $uri $uri/ /index.html;
    }

    location /api {
        root /var/www/back/public;
        try_files $uri $uri/ /index.php?$query_string;
        fastcgi_pass back:9000;
        fastcgi_index index.php;
        fastcgi_param SCRIPT_FILENAME $document_root$fastcgi_script_name;
        include fastcgi_params;
    }
}
