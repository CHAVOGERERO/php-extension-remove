# php-extension-remove

## APM 안에서 .php확장자 제거방법
<br/>
OS : UBUNTU 16.04 LTS<br/>
web Server : Apache/2.4.18<br/>
PHP : php 7.2.3

### 아파치 수정
수정할 부분
```
<Directory /var/www/>
        Options Indexes FollowSymLinks MultiViews
        AddType application/x-httpd-php .php
        AllowOverride All
        Require all granted
</Directory>
```

**MultiViews** 추가<br/>
**AddType application/x-httpd-php .php** 추가<br/>
**AllowOverride None -> AllowOverride All** 수정<br/>

전체 옵션에 대해서는 확인하지 못했다.<br/>
검색해서 찾아본 예시대로 추가 또는 수정을 했다.<br/>
<br/>
참고 사이트 : [http://jmoon.co.kr/m/107](http://jmoon.co.kr/m/107)