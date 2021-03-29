### Installation
```shell
bash <(curl -o .tmux.conf https://raw.githubusercontent.com/DoJoMi/init.tmux/master/.tmux.conf)
```
### Reload file
```shell
:source-file ~/tmux.conf       --> with vim
tmux source-file ~/tmux.conf   --> with tmux
^a r       --reload with tmux
```
### Basic usage (reconfigured from ctrl+b to ctrl+a)
```shell
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
 ```       
### Advanced options
```shell
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
```

### Plugins handled with [tpm](https://github.com/tmux-plugins/tpm)
```shell
# https://github.com/tmux-plugins
set -g @plugin 'tmux-plugins/tpm'
set -g @plugin 'tmux-plugins/tmux-sensible'
set -g @plugin 'jimeh/tmux-themepack'
set -g @themepack 'powerline/default/green'

# Initialize TMUX plugin manager (keep this line at the very bottom of tmux.conf)
run -b '~/.tmux/plugins/tpm/tpm'

^a I       --fetch plugins
^a alt+u   --uninstall plugins
```
