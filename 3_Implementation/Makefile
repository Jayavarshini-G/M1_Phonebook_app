SRC = src/main.c\
src/menu.c\
src/name.c\
src/find.c\
src/list.c\
src/exitfun.c\
src/deleted.c\

INC = -Iinc\

PROJECT_NAME = PHONEBOOK.out

$(PROJECT_NAME): $(SRC)
	gcc $(SRC) $(INC) -o $(PROJECT_NAME) -lncurses

run:$(PROJECT_NAME)
	./${PROJECT_NAME}
doc:
	make -C documentation

clean:
	rm -rf $(PROJECT_NAME) documentation/html

coverage:${PROJECT_NAME}
	gcc -fprofile-arcs -ftest-coverage $(SRC) $(INC) -o $(PROJECT_NAME)
	./${PROJECT_NAME}
	gcov -a src/menu.c src/name.c src/find.c src/list.c src/exitfun.c src/deleted.c 
