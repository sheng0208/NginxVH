# NginxVH 虛擬主機設置 (Mac)

## 1. nginx.conf 設定

>	#user  nobody;
>	worker_processes  1;
>	
>	#error_log  logs/error.log;
>	#error_log  logs/error.log  notice;
>	#error_log  logs/error.log  info;
>	
>	#pid        logs/nginx.pid;
>	
>	
>	events {
>	worker_connections  1024;
>	}
>	
>	
>	http {
>	include       mime.types;
>	default_type  application/octet-stream;
>	
>	#log_format  main  '$remote_addr - $remote_user [$time_local] "$request" '
>	\#                  '$status $body_bytes_sent "$http_referer" '
>	\#                  '"$http_user_agent" "$http_x_forwarded_for"';
>	
>	#access_log  logs/access.log  main;
>	
>	sendfile        on;
>	#tcp_nopush     on;
>	
>	#keepalive_timeout  0;
>	keepalive_timeout  65;
>	
>	
>	
>	include /usr/local/etc/nginx/conf.d/*.conf;
>	}

## 2. 在 usr/local/etc/nginx 目錄底下 新增一個`conf.d`資料夾