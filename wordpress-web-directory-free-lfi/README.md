# wordpress-web-directory-free-lfi
CVE-2024-3673漏洞利用
include在w2dc_renderTemplate函数被利用
![img01](./images/img01.png)
w2dc_renderTemplate函数通过w2dc_frontend_controller类的display方法调用
![img02](./images/img02.png)
![img03](./images/img03.png)
template参数是初始化时传入的
![img04](./images/img04.png)
![img05](./images/img05.png)
值是$_POST['template']
![img06](./images/img06.png)
最后构造请求wp_ajax_w2dc_controller_request
![img07](./images/img07.png)
![img08](./images/img08.png)
![img09](./images/img09.png)
