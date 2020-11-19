./configure --with-http\_ssl\_module --with-openssl=/usr/local/opt/openssl@1.1/

./configure: error: can not detect int size

在64位的机器上进行对nginx进行编译配置,居然报错error: can not detect int size,原来是加上了–with-cpu-opt选项.

[https://stackoverflow.com/questions/10568735/nginx-configure-error-can-not-detect-int-size](https://stackoverflow.com/questions/10568735/nginx-configure-error-can-not-detect-int-size)

[https://github.com/nginx/nginx](https://github.com/nginx/nginx)

$ ./auto/configure

$ make -j4

$sudo make install

