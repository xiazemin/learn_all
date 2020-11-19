Nginx的配置文件是以block的形式组织的，一个block通常使用大括号“{}”表示。block分为几个层级，整个配置文件为main层级，这是最大的层级；在main层级下可以有event、http等层级，而http中又会有server block，server block中可以包含location block。

Nginx本身支持多种模块，如HTTP模块、EVENT模块和MAIL模块



