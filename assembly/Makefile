run:
	docker compose run --rm assembly sh -c 'nasm -f elf64 -o ./src/main.o ./src/main.asm && ld ./src/main.o && ld ./src/main.o && ./a.out'

test:
	docker compose run --rm assembly sh -c 'nasm -f elf64 -o ./src/main.o ./src/main.asm && ld ./src/main.o && ld ./src/main.o && ./a.out'

update:
	docker compose build
