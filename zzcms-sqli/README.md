# zzcms-sqli
## CVE-2025-0565复现过程
定位到sql代码，上方是通过$_REQUEST获取的id，而inc/global.php只做了cookie/get/post的转义
![img01](./images/img01.png)
query函数没有对数据进行处理直接执行
![img02](./images/img02.png)
top.php中没有引入query.php，index.php中包含了top.php和conn.php，从index.php利用
![img03](./images/img03.png)
使用union注入，根据zzcms_user表对齐列
![img04](./images/img04.png)
延时注入需要zzcms_user表中有数据，否则mysql优化器会跳过sleep
![img05](./images/img05.png)
