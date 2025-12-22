all:	hello

hello:	valid.o
	$(CC) -o hello valid.o

clean:
	$(RM) valid.o

fclean:	clean
	$(RM) hello

re:	fclean all
