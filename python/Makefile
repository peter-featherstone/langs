run:
	docker compose run --rm python sh -c 'python3 main.py'

test:
	docker compose run --rm python sh -c 'pytest'

update:
	docker compose run --rm python sh -c 'uv pip compile --no-cache requirements.in' > requirements.txt
	docker compose build
