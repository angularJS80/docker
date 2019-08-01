docker exec -it nodejs /bin/bash
node app.js
오류나면 

vi /usr/local/bin/nd-try/middleware/mongodbConnection.js
접속정보 수정하고 

pm2 start app.js
