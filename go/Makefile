install:
	docker compose build --no-cache

run:
	docker compose run go /application

run-raw:
	docker compose run go sh -c 'go run .'

compile:
	docker compose build

update:
	docker compose build
	docker compose run go sh -c 'go mod tidy'
