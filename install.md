

# 사전 의존성 설치 
### GCC 등
```sudo apt-get install build-essential```

### pcre
```sudo apt-get install libpcre3 libpcre3-dev```

### zlib
```sudo apt-get install zlib1g zlib1g-dev```

### openssl
```sudo apt-get install openssl libssl-dev```

### geoip, 이미지필터, xslt 등
```sudo apt-get install libgeoip-dev libgd-dev libxslt-dev libxml2```



# 구성
```--prefix=설치될경로```
```--conf-path=conf파일위치```
```--error-log-path=에어로그위치```
```--http-log-path=엑세스로그위치```
```--user=유저명```
```--group=그룹명```

### SSL모듈 활성화
```--with-http_ssl_module```
### http/2 활성화
```--with-http_v2_module```
### 실제IP주소 모듈
```--with-http_realip_module```
### mp4 모듈
```--with-http_mp4_module```
### gzip 모듈
```--with-http_gzip_static_module```
### 서버 통계와 정보페이지 모듈
```--with-http_stub_status_module```
### 구글 성능도구 모듈
```--with-google_perftools_module```
### gunzip 모듈
```--with-http_gunzip_module```
### 인증모듈
```--with-http_auth_request_module```

<hr/>

# 예제
./configure --prefix=/DATA2/nginx-1.19.10 --user=www-data --group=www-data --with-http_ssl_module --with-http_realip_module

# 전체예제
./configure --prefix=/DATA2/nginx-1.19.10 --user=www-data --group=www-data --with-http_ssl_module --with-http_realip_module --with-http_addition_module --with-http_xslt_module --with-http_image_filter_module --with-http_geoip_module --with-http_sub_module --with-http_dav_module --with-http_flv_module --with-http_mp4_module --with-http_gzip_static_module --with-http_random_index_module --with-http_secure_link_module --with-http_stub_status_module --with-http_perl_module --with-http_degradation_module --with-http_gunzip_module --with-http_auth_request_module --with-http_v2_module

# 메일관련
./configure --prefix=/DATA2/nginx-1.19.10 --user=www-data --group=www-data --with-mail --with-mail_ssl_module