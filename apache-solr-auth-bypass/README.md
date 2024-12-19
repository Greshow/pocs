# apache-solr-auth-bypass
## 环境搭建
```javascript
docker pull solr:8.8
docker run -d -p 8983:8983 --name solr8 solr:8.8
docker exec -it solr8 bash // 前端新增core失败
solr create_core -c new_core -d _default // 进后台添加
```

## 身份验证绕过环境搞不定，改复现文件读取>_< ~~CVE-2024-45216漏洞利用~~
core name
![img01](./images/img01.png)
开启Remote Streaming
![img02](./images/img02.png)
读取文件
![img03](./images/img03.png)
