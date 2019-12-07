# Basic-Auth-in-nginx

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
