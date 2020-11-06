# autoindex
autoindex for Nginx
美化 Nginx 默认的目录文件 索引页

------

### 配置方法：

1. 复制 .autoindex 目录至 D:\websites\fulicat\
ps: D:\websites\fulicat\\.autoindex
  

2. 修改 nginx.conf 文件

```
server {

    # autoindex for nginx
    location ~ ^(.*)/$ {
        autoindex       on;
        autoindex_localtime on;
        autoindex_exact_size off;

        add_before_body /.autoindex/header.html;
        add_after_body /.autoindex/footer.html;
    }
}
```

------


# Screenshots:

### before:
![before](https://raw.githubusercontent.com/fulicat/autoindex/master/autoindex_before.png)

### after:
![after](https://raw.githubusercontent.com/fulicat/autoindex/master/autoindex_after.png)
