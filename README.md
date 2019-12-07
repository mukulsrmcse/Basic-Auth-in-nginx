# Basic-Auth-in-nginx

#Code change in default.conf file

server {
  2     listen       80;
  3     server_name  localhost;
  4 
  5     location / {
  6         root                 /usr/share/nginx/html;
  7         index                index.html;
  8         auth_basic           "Basic Authentication";
  9         auth_basic_user_file "/etc/registry/.htpasswd";
 10     }
 11 
 12 }
