Deployer is a PHP Application deployment system powered by Laravel 5.2, written & maintained by Stephen Ball.

Sample `docker-compose.yml`:
```yml
deployer:
  container_name: deployer
  image: sunfoxcz/deployer:0.1.1
  environment:
    - TZ=Europe/Prague
    - APP_DEBUG=true
    - APP_LOG=syslog
    - APP_KEY=base64:xxx
    - APP_URL=https://deployer.domain.tld
    - APP_TIMEZONE=Europe/Prague
    - JWT_SECRET=xxx
    - SOCKET_URL=https://deployer.domain.tld
    - DB_TYPE=mysql
    - DB_HOST=mysql.domain.tld
    - DB_DATABASE=deployer
    - DB_USERNAME=deployer
    - DB_PASSWORD=xxx
    - MAIL_FROM_ADDRESS=deployer@domain.tld
  ports:
    - "127.0.0.1:8091:80"

```

Env variables `APP_KEY` and `JWT_SECRET` will be generated if not given.

Default user after installation is `admin@example.com` and password is `password`.
