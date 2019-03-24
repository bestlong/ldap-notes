# 研究 LDAP - 使用 docker-compose 環境

目前組裝了下列功能

* OpenLDAP
* phpLDAPadmin
* LAM (LDAP Account Manager)

## 開始

啟動容器

```shell
docker-compose up -d
```

服務啟動後要做的基本設定，登入 openldap 容器

```shell
docker-compose exec openldap bash
```

匯入必要的 LDIF

再來就可以開瀏覽器

* 進入 phpLDAPadmin 主畫面
  * <http://localhost:8080/>
* 進入 LAM 主畫面
  * <http://localhost:8081/>
  * 要先進入右上角 LAM Configuration > Edit server profiles 修改設定
    * LAM Profile 密碼是 lam
  * General settings:
    * Server settings: ldap://localhost:389 改為 ldap://openldap:389
    * Tree suffix: dc=yourdomain,dc=org 改為 dc=example,dc=org
  * Language settings:
    * Default language: English (USA) 或 繁體中文
    * Time zone: Asia/Taipei
  * Security settings:
    * List of valid users: cn=Manager,dc=my-domain,dc=com 改為 cn=admin,dc=example,dc=org

用 Safari 瀏覽若出現無法打開網頁的錯誤(會被跳轉 https)，請改用 127.0.0.1 IP 當網址

登入 DN 是 cn=admin,dc=example,dc=org 密碼是 admin

如果需要進入 OpenLDAP 容器用命令列操作

```shell
docker-compose exec openldap bash
```

停止與移除容器 (請注意：目前尚未用到 Volume 掛載來保存資料，所以前項操作的結果會被刪除)

```shell
docker-compose down
```
