
installation
-----
	sudo yum install -y tmux \
	bash <(curl -o .tmux.conf https://raw.githubusercontent.com/DoJoMi/dottmux/master/.tmux.conf)

basic usage (reconfigured from ctrl+b to ctrl+a)
-----
        ^a ?        --show keys
        ^a c        --create new window --> changed to automatic rename window
        ^a ,        --rename window
        ^a n        --next window
        ^a p        --previous window   --> not longer available
        ^a d        --exit current window
        ^a "        --split h           --> changed to |
        ^a %        --split v           --> changed to _
        ^a t        --show time         --> fullscreen time in cyan
        ^a &        --del session
        
advanced options
-----
        
        ^a hjkl     --vim movements
        ^a HJKL     --resize window size
        
        ^a esc      --enter/exit copy mode
        ^a esc v    --start visual mode (V visual line)
        ^a esc v y  --yank into buffer
        ^a p        --previous window --> changed to paste buffer
        ^a -        --delete buffer 
     
        mouse key   --resize window size with mouse
        shift+mouse --copy/paste into tmux 
        
        tmux ls          --show sessions
        tmux a -t <name> --attach specific session

reconfigure file inside tmux session
------
        tmux ^a :source-file ~/.tmux.conf

plugins handled with [tpm](https://github.com/tmux-plugins/tpm)
------
        git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm
        echo -e "set -g @plugin 'nhdaly/tmux-scroll-copy-mode'"
        ~/.tmux/plugins/tpm/tpm
        ^a I       --fetch plugins
        ^a alt+u   --uninstall plugins

colour
------
        for i in {0..255} ; do
         printf "\x1b[38;5;${i}mcolour${i}\n"
        done

how it looks like
------
![image](https://raw.githubusercontent.com/DoJoMi/dottmux/master/tmux.png)

