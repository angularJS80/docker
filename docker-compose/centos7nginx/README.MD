--용도 : 프라이빗 도커 레지스트리를 위한 엔진엑스
--설정 : docker exec -it nginx /bin/bash 
vi /etc/nginx/sites-available
  172.31.34.84 를 물리아이피로 변경한다.

vi /etc/hosts
      물리아이피와 인증서의 도메인 주소 기록 
      nginx // nginx 시작해줘야 된다.

cp /etc/nginx/sslcert/server.crt /etc/pki/ca-trust/source/anchors/
update-ca-trust enable
update-ca-trust extract
