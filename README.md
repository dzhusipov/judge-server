# judge-server

### With HTTPS (SSL/TLS)
1. Install [Docker](https://docs.docker.com) and [Docker Compose](https://docs.docker.com/compose).
2. Download and extract release archive:
```
wget https://github.com/judge0/judge0/releases/download/v1.12.0/judge0-v1.12.0-https.zip
unzip judge0-v1.12.0-https.zip
```

3. Change directory to `judge0-v1.12.0-https`:
```
cd judge0-v1.12.0-https
```
4. Edit `docker-compose.yml` and change variables `VIRTUAL_HOST`, `LETSENCRYPT_HOST` and `LETSENCRYPT_EMAIL`.
5. Run all services and wait a few seconds until everything is initialized:
```
docker-compose up -d db redis
sleep 10s
docker-compose up -d
sleep 5s
```

6. Your instance of Judge0 v1.12.0 is now available at `https://<YOUR DOMAIN>`.
