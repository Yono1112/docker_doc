# docker

## only first
( docker run --name \$(NAME) -it ubuntu )
- docker run -itd --name \$(NAME) --mount type=bind,src=$(指定したいディレクトリ),target=/root ubuntu

## second
- docker ps -a →立ち上がってるけどstartしていない環境を確認
- docker start $(NAME) →\$(NAME)の環境を起動させる 
    - <!-- - docker attach $(NAME) -->
    - docker exec -it $\(NAME) /bin/bash → $\(NAME)の環境にbashでattachする、execはattachコマンドと違って仮想環境からexitした後もその環境がstartされたままになっている。attachはexitしたらもう一回startさせる必要あり。

## tips
- docker rm $(NAME)

# valgrind
- valgrind --tool=memcheck --log-file=$PWD/log_valgrind.txt $(実行したいコマンド)
