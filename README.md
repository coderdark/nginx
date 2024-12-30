# NGINX Server
It is a web server, reverse-proxy and forward-proxy

## Installing
+ Mac
  + [How to install homebrew](https://docs.brew.sh/Installation)
  + `brew install nginx`
+ Linux ([Raspberry PI](https://pimylifeup.com/raspberry-pi-nginx/))
  + `sudo apt install nginx`

## Starting
+ Mac
  + Brew
    + Start: `brew services start nginx`
    + Stop: `brew services stop nginx`
    + Reload: `brew services reload nginx`
  + nginx
    + Start: `nginx`
    + Stop: `nginx -s stop` - Fast Shutdown
    + Quit: `nginx -s quit` - Graceful Shutdown
    + Reload: `nginx -s reload`
    + Reload: `nginx -s reopen`
+ Linux
  + nginx
    + Start: `nginx`
    + Stop: `nginx -s stop` - Fast Shutdown
    + Quit: `nginx -s quit` - Graceful Shutdown
    + Reload: `nginx -s reload`
    + Reload: `nginx -s reopen`
   
## Commands
+ `kill -s <id>`  - to quit the process
+ `ps -ax | grep nginx` - list of running nginx processes
   
## View Index Page
+ Once you have the server running, point your browser to `localhost` or `localhost:8080` depending on how your server was setup.

## Configure nginx
To __test__ a configuration and also to know where the configuration is located at, type: `nginx -t`.   Type: `nginx -V` and it will provide the config and the path.

## Default Config
+ Port: `80`
+ Main Config Path: `/etc/nginx`
+ Main Config File: `nginx.conf`
+ Main HTML Path: `/usr/share/nginx/html`
+ Configs (Virtual Sites) `conf.d` or `sites-available`, depends on your setup
  + conf.d
    + Path: `/etc/nginx/conf.d`
    + Default Config: `default.conf`
  + sites-available
    + Path: `/etc/nginx/sites-available`
    + Path: `/etc/nginx/sites-enabled`
   
## Example Server Block
```
server {
    listen       80;
    listen  [::]:80;
    server_name  localhost;

    #access_log  /var/log/nginx/host.access.log  main;

    location / {
        root   /usr/share/nginx/html;
        index  index.html index.htm;
    }

    #error_page  404              /404.html;

    # redirect server error pages to the static page /50x.html
    #
    error_page   500 502 503 504  /50x.html;
    location = /50x.html {
        root   /usr/share/nginx/html;
    }

    # proxy the PHP scripts to Apache listening on 127.0.0.1:80
    #
    #location ~ \.php$ {
    #    proxy_pass   http://127.0.0.1;
    #}

    # pass the PHP scripts to FastCGI server listening on 127.0.0.1:9000
    #
    #location ~ \.php$ {
    #    root           html;
    #    fastcgi_pass   127.0.0.1:9000;
    #    fastcgi_index  index.php;
    #    fastcgi_param  SCRIPT_FILENAME  /scripts$fastcgi_script_name;
    #    include        fastcgi_params;
    #}

    # deny access to .htaccess files, if Apache's document root
    # concurs with nginx's one
    #
    #location ~ /\.ht {
    #    deny  all;
    #}
}

```
  
## Resources
+ [Nginx Missing Sites-available Directory | Better Stack Community](https://betterstack.com/community/questions/nginx-missing-site-available-directory/)
