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
==> Downloading https://homebrew.bintray.com/bottles/openssl%401.1-1.1.1h.catalina.bottle.tar.gz
Already downloaded: /Users/xiazemin/Library/Caches/Homebrew/downloads/4495e57344279a889f251b5431855ca33bf33b365d3c619e953c8390cfdc336b--openssl@1.1-1.1.1h.catalina.bottle.tar.gz
==> Reinstalling openssl@1.1
==> Pouring openssl@1.1-1.1.1h.catalina.bottle.tar.gz
==> Caveats
A CA file has been bootstrapped using certificates from the system
keychain. To add additional certificates, place .pem files in
  /usr/local/etc/openssl@1.1/certs

and run
  /usr/local/opt/openssl@1.1/bin/c_rehash

openssl@1.1 is keg-only, which means it was not symlinked into /usr/local,
because macOS provides LibreSSL.

If you need to have openssl@1.1 first in your PATH run:
  echo 'export PATH="/usr/local/opt/openssl@1.1/bin:$PATH"' >> /Users/xiazemin/.bash_profile

For compilers to find openssl@1.1 you may need to set:
  export LDFLAGS="-L/usr/local/opt/openssl@1.1/lib"
  export CPPFLAGS="-I/usr/local/opt/openssl@1.1/include"

For pkg-config to find openssl@1.1 you may need to set:
  export PKG_CONFIG_PATH="/usr/local/opt/openssl@1.1/lib/pkgconfig"

==> Summary
🍺  /usr/local/Cellar/openssl@1.1/1.1.1h: 8,067 files, 18.5MB
==> Upgrading 4 dependents:
freetds 1.2.6 -> 1.2.11, libpq 13.0_1 -> 13.1, openldap 2.4.55 -> 2.4.56, pango 1.46.2 -> 1.48.0
==> Upgrading libpq 13.0_1 -> 13.1
==> Downloading https://homebrew.bintray.com/bottles/libpq-13.1.catalina.bottle.tar.gz
==> Downloading from https://d29vzk4ow07wi7.cloudfront.net/394a2065cf06312fe23f56978cecdd3adc7f73bb6b2a3b9949cb7f3fba364ea2?response-content-dispo
######################################################################## 100.0%
==> Pouring libpq-13.1.catalina.bottle.tar.gz
==> Caveats
libpq is keg-only, which means it was not symlinked into /usr/local,
because conflicts with postgres formula.

If you need to have libpq first in your PATH run:
  echo 'export PATH="/usr/local/opt/libpq/bin:$PATH"' >> /Users/xiazemin/.bash_profile

For compilers to find libpq you may need to set:
  export LDFLAGS="-L/usr/local/opt/libpq/lib"
  export CPPFLAGS="-I/usr/local/opt/libpq/include"

For pkg-config to find libpq you may need to set:
  export PKG_CONFIG_PATH="/usr/local/opt/libpq/lib/pkgconfig"

==> Summary
🍺  /usr/local/Cellar/libpq/13.1: 2,269 files, 26.4MB
Removing: /usr/local/Cellar/libpq/13.0_1... (2,268 files, 26.4MB)
Removing: /Users/xiazemin/Library/Caches/Homebrew/libpq--13.0_1.catalina.bottle.tar.gz... (6.2MB)
==> Upgrading openldap 2.4.55 -> 2.4.56
==> Downloading https://homebrew.bintray.com/bottles/openldap-2.4.56.catalina.bottle.tar.gz
==> Downloading from https://d29vzk4ow07wi7.cloudfront.net/c51d24181e4291ece30b4ff8504f864bc4e0432a0dc85b64d6f4cac68b4f43dd?response-content-dispo
######################################################################## 100.0%
==> Pouring openldap-2.4.56.catalina.bottle.tar.gz
==> Caveats
openldap is keg-only, which means it was not symlinked into /usr/local,
because macOS already provides this software and installing another version in
parallel can cause all kinds of trouble.

If you need to have openldap first in your PATH run:
  echo 'export PATH="/usr/local/opt/openldap/bin:$PATH"' >> /Users/xiazemin/.bash_profile
  echo 'export PATH="/usr/local/opt/openldap/sbin:$PATH"' >> /Users/xiazemin/.bash_profile

For compilers to find openldap you may need to set:
  export LDFLAGS="-L/usr/local/opt/openldap/lib"
  export CPPFLAGS="-I/usr/local/opt/openldap/include"

==> Summary
🍺  /usr/local/Cellar/openldap/2.4.56: 329 files, 7.1MB
Removing: /usr/local/Cellar/openldap/2.4.55... (329 files, 7.1MB)
Removing: /Users/xiazemin/Library/Caches/Homebrew/openldap--2.4.55.catalina.bottle.tar.gz... (2.7MB)
==> Upgrading freetds 1.2.6 -> 1.2.11
==> Downloading https://homebrew.bintray.com/bottles/freetds-1.2.11.catalina.bottle.tar.gz
==> Downloading from https://d29vzk4ow07wi7.cloudfront.net/3f9c9217b97b0fc696ddf0e17322a19fc632d85aa5fc989eec6de81f5e92d017?response-content-dispo
######################################################################## 100.0%
==> Pouring freetds-1.2.11.catalina.bottle.tar.gz
🍺  /usr/local/Cellar/freetds/1.2.11: 1,259 files, 13.8MB
Removing: /usr/local/Cellar/freetds/1.2.6... (1,259 files, 13.7MB)
Removing: /Users/xiazemin/Library/Caches/Homebrew/freetds--1.2.6.catalina.bottle.tar.gz... (2.9MB)
==> Upgrading pango 1.46.2 -> 1.48.0
==> Downloading https://homebrew.bintray.com/bottles/pango-1.48.0.catalina.bottle.tar.gz
==> Downloading from https://d29vzk4ow07wi7.cloudfront.net/8efc7e43fabedde9160927212857a7fa950a0ee4768374a5f36fc7b7a4e79c44?response-content-dispo
######################################################################## 100.0%
==> Pouring pango-1.48.0.catalina.bottle.tar.gz
🍺  /usr/local/Cellar/pango/1.48.0: 64 files, 3MB
Removing: /usr/local/Cellar/pango/1.46.2... (64 files, 2.9MB)
Removing: /Users/xiazemin/Library/Caches/Homebrew/pango--1.46.2.catalina.bottle.tar.gz... (728KB)
==> Checking for dependents of upgraded formulae...
==> No broken dependents found!
==> Caveats
==> openssl@1.1
A CA file has been bootstrapped using certificates from the system
keychain. To add additional certificates, place .pem files in
  /usr/local/etc/openssl@1.1/certs

and run
  /usr/local/opt/openssl@1.1/bin/c_rehash

openssl@1.1 is keg-only, which means it was not symlinked into /usr/local,
because macOS provides LibreSSL.

If you need to have openssl@1.1 first in your PATH run:
  echo 'export PATH="/usr/local/opt/openssl@1.1/bin:$PATH"' >> /Users/xiazemin/.bash_profile

For compilers to find openssl@1.1 you may need to set:
  export LDFLAGS="-L/usr/local/opt/openssl@1.1/lib"
  export CPPFLAGS="-I/usr/local/opt/openssl@1.1/include"

For pkg-config to find openssl@1.1 you may need to set:
  export PKG_CONFIG_PATH="/usr/local/opt/openssl@1.1/lib/pkgconfig"

==> libpq
libpq is keg-only, which means it was not symlinked into /usr/local,
because conflicts with postgres formula.

If you need to have libpq first in your PATH run:
  echo 'export PATH="/usr/local/opt/libpq/bin:$PATH"' >> /Users/xiazemin/.bash_profile

For compilers to find libpq you may need to set:
  export LDFLAGS="-L/usr/local/opt/libpq/lib"
  export CPPFLAGS="-I/usr/local/opt/libpq/include"

For pkg-config to find libpq you may need to set:
  export PKG_CONFIG_PATH="/usr/local/opt/libpq/lib/pkgconfig"

==> openldap
openldap is keg-only, which means it was not symlinked into /usr/local,
because macOS already provides this software and installing another version in
parallel can cause all kinds of trouble.

If you need to have openldap first in your PATH run:
  echo 'export PATH="/usr/local/opt/openldap/bin:$PATH"' >> /Users/xiazemin/.bash_profile
  echo 'export PATH="/usr/local/opt/openldap/sbin:$PATH"' >> /Users/xiazemin/.bash_profile

For compilers to find openldap you may need to set:
  export LDFLAGS="-L/usr/local/opt/openldap/lib"
  export CPPFLAGS="-I/usr/local/opt/openldap/include"
```



