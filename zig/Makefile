install:
	docker compose build --no-cache

run:
	docker compose run --rm zig sh -c 'zig run src/main.zig'

compile:
	docker compose run --rm zig sh -c 'zig build-exe src/main.zig'
