all:	hello

hello:	invalid.o
	$(CC) -o hello invalid.o

clean:
	$(RM) invalid.o

fclean:	clean
	$(RM) hello

re:	fclean all

.PHONY: all clean fclean re
