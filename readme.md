## 🛠️ Generate Self-Signed Certificates

```bash
mkdir -p certs
openssl req -x509 -newkey rsa:4096 -nodes \
  -keyout certs/server.key \
  -out certs/server.crt \
  -days 365 \
  -subj "/CN=localhost"
```

## 🚀 Run Docker Compose

```bash
docker-compose --env-file .env up --build
```

## 🌐 Access URLs

| Service    | URL                   |
| ---------- | --------------------- |
| Next.js    | https://next.local    |
| WordPress  | https://wp.local      |
| Adminer    | http://localhost:8081 |
| PostgreSQL | localhost:5432        |
| MySQL      | localhost:3306        |

> ⚠️ **Accept the browser certificate warning** to access HTTPS services.
