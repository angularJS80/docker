도메인 인증 할때 docker-compose 에 80 포트 열어 둬야 한다. 인증 주체에서 80으로 들어온다. 
이때 data/cerbot 이하에 경로 는 nginx 의 location 에 설정에 의해 
인증주체가 호출하게 되는 url 이 설정되어 진다. 

그러므로 nginx 먼저 띄워둔 상태에서 ( 띄울려면 기존에 443 ssl 설정을 모두 주석 처리)

init-letencrypt.sh 에서 example.org 을 원하는 도메인으로 변경
init-letencrypt.sh 1회 실행 하여 인증서 발급 

docker registr로 이용시 /data/nginx/config/sites-available/docker_registry_htpasswd 참고
docker-compose up  


ref : https://medium.com/@pentacent/nginx-and-lets-encrypt-with-docker-in-less-than-5-minutes-b4b8a60d3a71

angular / vueJs 빌드가 필요한 깃헙 소스 빌드를 쉘스크립트로 작성하고
배포 결과물을 dockerFile에서 복사하게 한후 compose up 하도록 구상.. 


