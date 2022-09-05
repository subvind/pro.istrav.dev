pro.istrav.dev
========
fleet management software

source code:
- library: https://github.com/trabur/fleet-optimizer
- server: https://github.com/trabur/pro.istrav.dev
- clients:
  - browser: https://github.com/trabur/istrav.pro
  - mobile: coming soon!

apps:
- osrm: https://osrm.istrav.dev
- database: https://couchdb.istrav.dev
- server: https://pro.istrav.dev
- clients:
  - browser: https://istrav.pro
  - mobile: coming soon!

backend tech:
- OSRM server for calculating Matrix Distances
- socket.io server for live GPS tracking
- CouchDB server for rxdb.info/replication-couchdb.html

## TypeScript Framework
NestJS: https://github.com/nestjs/nest

## Installation
```bash
$ npm install
```

## Running the app
```bash
# development
$ npm run start

# watch mode
$ npm run start:dev

# production mode
$ npm run start:prod
```

## Test
```bash
# unit tests
$ npm run test

# e2e tests
$ npm run test:e2e

# test coverage
$ npm run test:cov
```

## Production
```bash
# firewall
$ sudo ufw allow 1337/tcp
$ sudo ufw reload

# start
$ PORT=1337 pm2 start dist/main.js --update-env --name="pro"

# stop
$ pm2 stop dist/main.js --name="pro"

# logs
$ pm2 logs pro

# delete
$ pm2 delete pro

# list
$ pm2 status

# Generate Startup Script
$ pm2 startup

# Freeze your process list across server restart
$ pm2 save

# Remove Startup Script
$ pm2 unstartup

# after code change
$ pm2 reload all
```