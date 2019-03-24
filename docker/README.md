# 研究 LDAP - 使用 docker-compose 環境

啟動容器

```shell
docker-compose up -d
```

服務啟動後就可以開瀏覽器

* 進入 phpLDAPadmin 主畫面
  * <http://localhost:8080/>
* 進入 LAM 主畫面開瀏覽器
  * <http://localhost:8081/>
* 用 Safari 瀏覽會出現無法打開網頁的錯誤(會被跳轉 https)，請改用 127.0.0.1 IP 當網址

登入 DN 是 cn=admin,dc=example,dc=org 密碼是 admin

如果需要進入 OpenLDAP 容器用命令列操作

```shell
docker-compose exec openldap bash
```

停止與移除容器

```shell
docker-compose down
```
