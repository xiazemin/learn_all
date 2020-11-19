Nginx的配置文件是以block的形式组织的，一个block通常使用大括号“{}”表示。block分为几个层级，整个配置文件为main层级，这是最大的层级；在main层级下可以有event、http等层级，而http中又会有server block，server block中可以包含location block。

Nginx本身支持多种模块，如HTTP模块、EVENT模块和MAIL模块

[https://www.evanmiller.org/nginx-modules-guide.html](https://www.evanmiller.org/nginx-modules-guide.html)

[https://www.kancloud.cn/kancloud/master-nginx-develop/51800](https://www.kancloud.cn/kancloud/master-nginx-develop/51800)

```
/* Directives */
static ngx_command_t ngx_http_echo_commands[] = {
 { ngx_string("echo"),
 NGX_HTTP_LOC_CONF|NGX_CONF_TAKE1,
 ngx_http_echo,
 NGX_HTTP_LOC_CONF_OFFSET,
 offsetof(ngx_http_echo_loc_conf_t, ed),
 NULL },
 ngx_null_command
};
/* Http context of the module */
static ngx_http_module_t ngx_http_echo_module_ctx = {
 NULL, /* preconfiguration */
 NULL, /* postconfiguration */
 NULL, /* create main configuration */
 NULL, /* init main configuration */
 NULL, /* create server configuration */
 NULL, /* merge server configuration */
 ngx_http_echo_create_loc_conf, /* create location configration */
 ngx_http_echo_merge_loc_conf /* merge location configration */
};
/* Module */
ngx_module_t ngx_http_echo_module = {
 NGX_MODULE_V1,
 &ngx_http_echo_module_ctx, /* module context */
 ngx_http_echo_commands, /* module directives */
 NGX_HTTP_MODULE, /* module type */
 NULL, /* init master */
 NULL, /* init module */
 NULL, /* init process */
 NULL, /* init thread */
 NULL, /* exit thread */
 NULL, /* exit process */
 NULL, /* exit master */
 NGX_MODULE_V1_PADDING
};
```



