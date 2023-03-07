# docker

## only first
<!-- - docker run --name $(NAME) -it ubuntu -->
- docker run -itd --name val --mount type=bind,src=/Users/yumaohno/Documents/42tokyo,target=/root ubuntu

## second
- docker ps -a
- docker start $(NAME)
<!-- - docker attach $(NAME) -->
- docker exec -it $(NAME) /bin/bash

## tips
- docker rm $(NAME)

# valgrind
- valgrind --tool=memcheck --log-file=$PWD/log_valgrind.txt ./push_swap 1 2 3
