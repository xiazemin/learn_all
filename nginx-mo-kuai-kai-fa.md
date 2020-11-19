curl -O [http://nginx.org/download/nginx-1.0.0.tar.gz](http://nginx.org/download/nginx-1.0.0.tar.gz)

tar -zxvf nginx-1.0.0.tar.gz

cd nginx-1.0.0

```
./configure: error: SSL modules require the OpenSSL library.
You can either do not enable the modules, or install the OpenSSL library
into the system, or build the OpenSSL library statically from the source
with nginx by using --with-openssl=<path> option.
```

$ brew reinstall openssl

```

If you need to have libpq first in your PATH run:
  echo 'export PATH="/usr/local/opt/libpq/bin:$PATH"' >> /Users/xiazemin/.bash_profile

For compilers to find libpq you may need to set:
  export LDFLAGS="-L/usr/local/opt/libpq/lib"
  export CPPFLAGS="-I/usr/local/opt/libpq/include"

For pkg-config to find libpq you may need to set:
  export PKG_CONFIG_PATH="/usr/local/opt/libpq/lib/pkgconfig"
```



