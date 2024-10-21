# NGINX Server

## Installing
+ Mac
  + [How to install homebrew](https://docs.brew.sh/Installation)
  + `brew install nginx`
+ Linux (Raspberry PI)
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
