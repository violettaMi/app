# README

This Rails 7.1 app is deployed to AWS EC2 with Docker and Nginx.
The gem `prometheus-client` is added to config monitoring via Prometheus & Grafana.

Commands:

`docker build -t app .`
`docker volume create app-storage`
`docker run --rm -it -v app-storage:/rails/storage -p 3000:3000 --env RAILS_MASTER_KEY=<config/master.key> app`
