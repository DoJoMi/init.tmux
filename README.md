
installation
-----
	
	sudo yum install -y tmux \
	bash <(curl -o .tmux.conf https://raw.githubusercontent.com/DoJoMi/dottmux/master/.tmux.conf)


usage
-----
        ^a ,   --rename window
        ^a n   --next window
        ^a p   --previous window
        ^a d   --exit current window
        ^a "   --split horizontally -->  changed to  |
        ^a %   --split pane vertically --> changed to -
        ^a t   --show time

        tmux attach 


reconfigure file
------
        tmux ^a :source-file ~/.tmux.conf


colour
------
        for i in {0..255} ; do
         printf "\x1b[38;5;${i}mcolour${i}\n"
        done
