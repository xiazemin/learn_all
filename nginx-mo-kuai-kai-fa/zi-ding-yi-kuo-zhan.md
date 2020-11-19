./auto/configure --prefix=/usr/local/nginx --add-module=./ngx\_http\_hello\_module

$ make -j4

$sudo make install

vi /usr/local/nginx/conf/nginx.conf

/usr/local/nginx/sbin/nginx

curl[http://127.0.0.1/hello](#)

hello nginx!



