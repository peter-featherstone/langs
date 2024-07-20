run:
	docker compose run --no-deps scripts sh -c 'python3 main.py'

install:
	docker compose build --no-cache

update:
	docker compose run --no-deps scripts sh -c 'uv pip compile --no-cache requirements.in' > requirements.txt
	docker compose build
