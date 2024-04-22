install:
	docker compose build --no-cache

run:
	docker compose run rust sh -c 'cargo run .'

compile:
	docker compose run rust sh -c 'cargo build'

format:
	docker compose run rust sh -c 'cargo fmt'

check:
	docker compose run rust sh -c 'cargo check'

update:
	docker compose build
	docker compose run rust sh -c 'cargo update'

docs:
	cargo doc --open
