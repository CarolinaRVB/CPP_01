# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: crebelo- <crebelo-@student.42lisboa.com    +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2024/06/25 08:55:46 by crebelo-          #+#    #+#              #
#    Updated: 2024/06/25 10:56:18 by crebelo-         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

NAME := ex01

SRC := Zombie.cpp \
	   ZombieHorde.cpp \
	   main.cpp 

OBJ := $(SRC:.cpp=.o)

CC := c++

CFLAGS := -Wall -Wextra -Werror -std=c++98

GREEN := \033[0;32m

all: $(OBJ) $(NAME)

$(OBJ): %.o: %.cpp
	@$(CC) $(CFLAGS) -c $< -o $@

$(NAME): $(OBJ)
	@echo "$(GREEN) Compiling Zombie Horde creator ... "
	@$(CC) $(CFLAGS) $(OBJ) -o $(NAME)
	@echo "$(GREEN) Done! "

clean:
	@rm -f $(OBJ)

fclean: clean
	@rm -f $(NAME)

re: fclean all

.phony: all clean fclean re
