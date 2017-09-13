# Nginx-Puma-Sinatra Setup

See [nginx-puma-sinatra](https://github.com/p8952/nginx-puma-sinatra) repo for reference on setup.

## nginx.conf
After copying `config/nginx.conf` to `/etc/nginx/nginx.conf`, needed to change user in `nginx.conf` to root root. Not ideal and should find a workaround for this in the future. Also updated all relevant fields in config to use /home/ec2-user/heimdall_dev as a base.

## Config files
Moved puma.rb and config.ru to same dir as heimdall and altered config.ru to require './heimdall.rb' and run App.

## Heimdall
Changed heimdall to heimdall.rb and added class that App that inherits from sinatra base around sinatra code.

