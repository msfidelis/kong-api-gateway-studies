.PHONY: db build migration run up
build:
	docker-compose build
db: 
	docker-compose up -d kong-database

migration: 
	docker-compose run --rm kong-gateway kong migrations bootstrap

run: db migration
	docker-compose up 