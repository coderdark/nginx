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
+ Config Path: `/etc/nginx`
+ Config File: `nginx.conf`
+ HTML Path: `/usr/share/nginx/html`
