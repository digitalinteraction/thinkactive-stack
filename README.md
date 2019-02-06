# Automagical Nginx Reverse Proxy stack

A [Docker](https://www.docker.com) stack that automatically generates nginx to reverse-proxy http(s) traffic to you containers,
Setup using (robb-j/common)[https://github.com/robb-j/common/tree/master/web-stack]

## Simple Deploy

```bash
# Where `dev-api` and `dev-web` are the containers to be restarted
ssh root@thinkactive.io deploy dev-api dev-web
```

## Manual Deploy

```bash
# Go to the directory
cd /srv/apps

# Pull the latest changes
git pull

# Restart containers
docker-compose up -d
```

## Api Commands

```bash
# Run Migrations
dc exec dev-api npx sequelize db:seed:all

# Run Seeds
dc exec dev-api npx sequelize db:seed:all
```