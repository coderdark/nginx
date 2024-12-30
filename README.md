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
    + Stop: `nginx -s stop`
    + Reload: `nginx -s reload`
+ Linux
  + nginx
    + Start: `nginx`
    + Stop: `nginx -s stop`
    + Reload: `nginx -s reload`
   
## View Index Page
+ Once you have the server running, point your browser to `localhost:8080`

## Configure nginx
To __test__ a configuration and also to know where the configuration is located at, type: `nginx -t`.   Type: `nginx -V` and it will provid the config and the path.
