all:	hello

hello:	invalid.o
	$(CC) -o hello invalid.o

clean:
	$(RM) hello.o

fclean:	clean
	$(RM) hello

re:	fclean all
