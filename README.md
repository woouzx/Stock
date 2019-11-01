# Stock
Made some.

# Test
test 1

# test
test 2

#some thing here
server {
    listen       443;
    server_name  xxx.com;

    charset utf-8;
    #access_log  /var/log/nginx/host.access.log  main;
    
    ssl on;
    ssl_certificate   cert/xxxx.pem;
    ssl_certificate_key  cert/xxxx.key;
    ssl_session_timeout 5m;
    ssl_ciphers ....
    ssl_protocols TLSv1 TLSv1.1 TLSv1.2;
    ssl_prefer_server_ciphers on;

    location / {
        include uwsgi_params;
        uwsgi_pass unix:/tmp/uwsgi.sock;
    }
}
