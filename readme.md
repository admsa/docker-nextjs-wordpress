mkdir -p certs
openssl req -x509 -newkey rsa:4096 -nodes \
 -keyout certs/server.key \
 -out certs/server.crt \
 -days 365 \
 -subj "/CN=localhost"

docker-compose --env-file .env up --build

Next.js https://next.local
WordPress https://wp.local
Adminer http://localhost:8081
PostgreSQL localhost:5432
MySQL localhost:3306

Accept browser certificate warning to access HTTPS
