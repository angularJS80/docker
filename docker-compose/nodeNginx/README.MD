example.org 을 원하는 도메인으로 변경
docker registr로 이용시 /data/nginx/config/sites-available/docker_registry_htpasswd 참고
init-letencrypt.sh 1회 실행 하여 인증서 발급 이후 docker-compose up  


ref : https://medium.com/@pentacent/nginx-and-lets-encrypt-with-docker-in-less-than-5-minutes-b4b8a60d3a71

angular / vueJs 빌드가 필요한 깃헙 소스 빌드를 쉘스크립트로 작성하고
배포 결과물을 dockerFile에서 복사하게 한후 compose up 하도록 구상.. 
