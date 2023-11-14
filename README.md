# Oxidized
Oxidized is a network device configuration backup tool. It's a RANCID replacement!

#### Configure settings
- To configure storage configs (text file or git) you need edit the *output* section in file ./config/oxidized/config_example
- Update information in router.db file.

Copy file config/oxidized/config_example to config/oxidized/config
Copy file config/oxidized/router.db_example to config/oxidized/router.db

## Oxidized in docker

For start oxidized container execute:
*docker run -d -v $(pwd)/config/oxidized:/home/oxidized/.config/oxidized -p 8080:8888/tcp oxidized/oxidized:0.29.1-30-g52c1f98*

Check config status http://localhost:8080


## Oxidized in docker compose
To add authentication in web-interface you need run docker composer with nginx basic authentication:
1. Create user/password file: htpasswd -c ./config/nginx/.htpasswd <username>
2. Run docker-compose in deatach mode: docker-compose up -d

Check config status http://localhost:8080

