# LDAP (Lightweight Directory Access Protocol) 輕型目錄存取協定

集中帳號管理，很多軟體系統都支援 LDAP 服務

## 軟體資源

* LDAP 服務
  * [OpenLDAP](https://www.openldap.org)
  * [ApacheDS](https://directory.apache.org/apacheds/)
* 工具
  * [phpLDAPadmin](http://phpldapadmin.sourceforge.net/wiki/index.php/Main_Page)
    * 用 PHP 開發，不過很久沒發佈新版本了
  * [Apache Directory Studio](https://directory.apache.org/studio/)
    * 應該是用 Eclipse
  * [LDAP Account Manager (LAM)](https://www.ldap-account-manager.org/lamcms/)
    * <https://sourceforge.net/projects/lam/>
    * <https://github.com/LDAPAccountManager/lam>
    * 用 PHP 開發
    * 在 ubuntu 可用 `apt-get install ldap-account-manager` 指令安裝

## LDAP 會使用到的網路埠

* 389 明碼傳輸
* 636 TLS/SASL 加密傳輸

## 用 Docker compose 環境研究

要到 docker 目錄下操作
