NAME = philo
SRCS = main.c \
		ft_safe_atoi.c \
		supervisor_thread.c \
		error.c \
		exit.c \
		mutex.c \
		initialization.c \
		utils.c \
		thread.c \
		forks.c \
		arguments.c \
		philosophers_utils.c \
		philosophers.c

OBJS = $(SRCS:.c=.o)
HEADER = philosophers.h
FLAGS =  -Wall -Wextra -Werror -pthread -g
CC = cc

ifdef CHECK
	FLAGS = -Wall -Wextra -g -fsanitize=thread
endif

all : $(NAME)

$(NAME) : $(OBJS)
	$(CC) $(FLAGS) $(OBJS) -o $(NAME)

%.o : %.c $(HEADER)
	$(CC) $(FLAGS) -c $< -o $@

clean :
	rm -f $(OBJS)

fclean : clean
	rm -f $(NAME)


re : fclean all

.PHONY: all fclean clean re
