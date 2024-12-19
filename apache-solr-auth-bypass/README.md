# apache-solr-auth-bypass
## 环境搭建
```javascript
docker pull solr:8.8
docker run -d -p 8983:8983 --name solr8 solr:8.8
docker exec -it solr8 bash
solr create_core -c new_core -d _default // 前端新增core admin失败
```

## CVE-2024-45216漏洞利用
