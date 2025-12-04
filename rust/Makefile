install:
	docker compose build --no-cache

run:
	docker compose run --rm rust sh -c 'cargo run .'

compile:
	docker compose run --rm rust sh -c 'cargo build'

test:
	docker compose run --rm rust sh -c 'cargo test'

update:
	docker compose run --rm rust sh -c 'cargo update'
