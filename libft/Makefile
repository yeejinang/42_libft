# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: yang <yang@student.42kl.edu.my>            +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2021/05/20 17:54:25 by yang              #+#    #+#              #
#    Updated: 2021/05/23 17:30:26 by yang             ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

NAME		= libft.a

CC			= gcc

CFLAGS		= -Wall -Wextra -Werror

SRCS		= ft_memset.c ft_bzero.c ft_memcpy.c ft_memccpy.c \
				ft_memmove.c ft_memchr.c ft_memcmp.c ft_strlen.c \
				ft_strlcpy.c ft_strlcat.c ft_strchr.c ft_strrchr.c \
				ft_strnstr.c ft_strncmp.c ft_atoi.c ft_isalpha.c \
				ft_isdigit.c ft_isalnum.c ft_isascii.c ft_isprint.c \
				ft_toupper.c ft_tolower.c ft_calloc.c ft_strdup.c \
				ft_substr.c ft_strjoin.c ft_strtrim.c ft_split.c \
				ft_itoa.c ft_strmapi.c ft_putchar_fd.c ft_putstr_fd.c \
				ft_putendl_fd.c ft_putnbr_fd.c

OBJS		= $(SRCS:.c=.o)

BONUS		= ft_lstnew.c ft_lstadd_front.c ft_lstsize.c \
				ft_lstlast.c ft_lstadd_back.c ft_lstdelone.c \
				ft_lstclear.c ft_lstiter.c ft_lstmap.c

BONUS_OBJS	= $(BONUS:.c=.o)

all:		$(NAME)

$(NAME):	$(OBJS)
			ar rcs $(NAME) $(OBJS)

bonus:		$(OBJS) $(BONUS_OBJS)
			ar rcs $(NAME) $(OBJS) $(BONUS_OBJS)

norm:		
			norminette -R CheckForbiddenSourceHeader *.c
			norminette -R CheckDefine *.h

so:
			$(CC) -fPIC $(CFLAGS) $(SRCS) $(BONUS)
			gcc -shared -o libft.so $(OBJS) $(BONUS_OBJS)

clean:
			rm -f *.o

fclean:		clean
			rm -f $(NAME)

re:			fclean $(NAME)

.PHONY:		all clean fclean re bonus norm so
