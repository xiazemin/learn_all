$ ps aux \|grep nginx

xiazemin         74839   0.0  0.0  4268284    672 s003  S+    5:41下午   0:00.00 grep nginx

xiazemin         74835   0.0  0.0  4301000   1012   ??  S     5:41下午   0:00.00 nginx: worker process

xiazemin         74784   0.0  0.0  4300560   1312   ??  Ss    5:34下午   0:00.01 nginx: master process nginx

$ nginx -s reload 重启worker进程

$ ps aux \|grep nginx

xiazemin         74843   0.0  0.0  4268284    672 s003  S+    5:41下午   0:00.00 grep nginx

xiazemin         74841   0.0  0.0  4301000   1028   ??  S     5:41下午   0:00.00 nginx: worker process

xiazemin         74784   0.0  0.0  4300560   1432   ??  Ss    5:34下午   0:00.01 nginx: master process nginx

$ nginx -s reopen 重新打开日志文件

$ ps aux \|grep nginx

xiazemin         74846   0.0  0.0  4285692    700 s003  S+    5:42下午   0:00.00 grep nginx

xiazemin         74841   0.0  0.0  4301000   1080   ??  S     5:41下午   0:00.00 nginx: worker process

xiazemin         74784   0.0  0.0  4300560   1432   ??  Ss    5:34下午   0:00.01 nginx: master process nginx

$ vi /usr/local/etc/nginx/nginx.conf

```
location ~ \.php$ {
    root           html;
    fastcgi_pass   127.0.0.1:9000;
    fastcgi_index  index.php;
   #fastcgi_param  SCRIPT_FILENAME  /scripts$fastcgi_script_name;
    fastcgi_param SCRIPT_FILENAME $document_root$fastcgi_script_name;
   include        fastcgi_params;
}
```

```
sudo cp /private/etc/php-fpm.conf.default /private/etc/php-fpm.conf
```

/private/etc/php-fpm.conf



