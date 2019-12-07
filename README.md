# Basic-Auth-in-nginx
# https://docs.nginx.com/nginx/admin-guide/security-controls/configuring-http-basic-authentication/#complete-example
#Code change in default.conf file

server {
      listen       80;
      server_name  localhost;
  
      location / {
          root                 /usr/share/nginx/html;
          index                index.html;
          auth_basic           "Basic Authentication";
          auth_basic_user_file "/etc/registry/.htpasswd";
      }
  
  }
