Get latest docker.
Get latest docker-compose.

`docker-compose up -d`
`docker exec -it matrixriot_matrix_1 /start.sh generate`

Review config for all services.

Restart services if config was altered.
`docker-compose restart`

Create new local SSL cert if needed (or use Letsencrypt if IP is public)
`openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout ./etc/nginx/cert/localhost/privkey.pem -out ./etc/nginx/cert/localhost/fullchain.pem -subj /CN=localhost`

If this server is going public, add Letsencrypt certs and change the Nginx conf.
