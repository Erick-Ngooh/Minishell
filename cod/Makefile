# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: engooh <engooh@student.42.fr>              +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2022/06/07 11:25:28 by engooh            #+#    #+#              #
#    Updated: 2022/07/09 03:05:40 by engooh           ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

SRC = parsing/start.c
OBJ = ${SRC:%.c=%.o}
CFLAG = -g3 -Wall -Wextra -Werror -lreadline
DEPENDENCE = ./share/libft

all: libft minishell

libft:
	make -C $(DEPENDENCE)

minishell: $(OBJ)
	gcc $(CFLAG) $(OBJ) -o $@  

fsanthread: $(OBJ)
	gcc -fsanitize=thread $(CFLAG) $(OBJ) -o minishell

fsanadress: $(OBJ)
	gcc -fsanitize=address $(CFLAG) $(OBJ) -o minishell

bonus: $(OBJ_BONUS)
	gcc $(CFLAG) $(OBJ_BONUS) -o minishell

fsanbonusthread: $(OBJ_BONUS)
	gcc -fsanitize=address $(CFLAG) $(OBJ_BONUS) -o minishell

fsanbonusadress: $(OBJ_BONUS)
	gcc -fsanitize=thread $(CFLAG) $(OBJ_BONUS) -o minishell

%.o: %.c
	gcc $(CFLAG) -c $^ -o $@ 

cleanbonus:	
	rm src_bonus/*.o

clean: 
	make clean -C $(DEPENDENCE)
	rm -f $(OBJ)

fleanbonus:
	rm -f src_bonus/*.o

fclean: clean 
	rm -f minishell

re: fclean all

.PHONY: all fclean clean re bonus
