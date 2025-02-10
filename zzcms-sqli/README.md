# zzcms-sqli
CVE-2025-0565复现过程
定位到sql代码
![img01](./images/img01.png)
query函数
![img02](./images/img02.png)
top.php中没有引入query.php，index.php中包含了top.php和conn.php，从index.php利用
![img03](./images/img03.png)
使用union注入，根据zzcms_user表对齐列
![img04](./images/img04.png)
延时注入需要zzcms_user表中有数据，否则mysql优化器会跳过sleep
![img05](./images/img05.png)
