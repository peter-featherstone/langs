run:
	docker compose run --rm go sh -c 'go run .'

test:
	docker compose run --rm go sh -c 'go run .'

update:
	docker compose build
	docker compose run --rm go sh -c 'go mod tidy'
