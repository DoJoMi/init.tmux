
installation
-----
	
	sudo yum install -y tmux \
	bash <(curl -o .tmux.conf https://raw.githubusercontent.com/DoJoMi/dottmux/master/.tmux.conf)


usage
-----
	^a ?      --show keys
        ^a ,      --rename window
        ^a n      --next window
        ^a p      --previous window
        ^a d      --exit current window
        ^a "      --split h -->  changed to |
        ^a %      --split v -->  changed to -
        ^a t      --show time
        ^a &      --k old sessions
        ^a hjkl   --vim movements
        ^a HJKL   --resize window size
        mouse key --resize window size
        
        tmux ls          --show sessions
        tmux a -t <name> --attach specific session

reconfigure file inside tmux session
------
        tmux ^a :source-file ~/.tmux.conf

colour
------
        for i in {0..255} ; do
         printf "\x1b[38;5;${i}mcolour${i}\n"
        done

how it looks like
------
![image](https://raw.githubusercontent.com/DoJoMi/dottmux/master/tmux.png)

