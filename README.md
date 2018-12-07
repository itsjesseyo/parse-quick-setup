# parse-quick-setup
uses yongjhih docker images to setup prase server

#example usage from 
https://github.com/yongjhih/docker-parse-server/blob/master/ADVANCE.md#how-to-setup-ssl-with-letsencrypt



$ git clone https://github.com/yongjhih/docker-parse-server
$ cd docker-parse-server

$ USER1=yongjhih \
  USER1_PASSWORD=yongjhih \
  PARSE_DASHBOARD_VIRTUAL_HOST=parse.example.com \
  PARSE_DASHBOARD_LETSENCRYPT_HOST=parse.example.com \
  PARSE_DASHBOARD_LETSENCRYPT_EMAIL=yongjhih@example.com \
  PARSE_SERVER_VIRTUAL_HOST=api.example.com \
  PARSE_SERVER_LETSENCRYPT_HOST=api.example.com \
  PARSE_SERVER_LETSENCRYPT_EMAIL=yongjhih@example.com \
  SERVER_URL=https://api.example.com/parse \
  APP_ID=YOUR_APP_ID MASTER_KEY=YOUR_MASTER_KEY docker-compose -f docker-compose-le.yml up
