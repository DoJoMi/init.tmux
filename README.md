### Installation
```shell
➜ tmux -V
tmux 3.1c
```
```shell
git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm && \
bash <(curl -o .tmux.conf https://raw.githubusercontent.com/DoJoMi/init.tmux/master/.tmux.conf)
# tmux
# ^b I
```
### Reload file
```shell
:source-file ~/tmux.conf       --> with vim
tmux source-file ~/tmux.conf   --> with tmux
^a r       --reload with tmux
```
### Basic usage (reconfigured from ctrl+b to ctrl+a)
```shell

# change prefix key inside the .tmux.conf for your needs
#unbind C-b
#set -g prefix C-a


^b ?        --show keys
^b c        --create new window --> changed to automatic rename window
^b ,        --rename window
^b n        --next window
^b p        --previous window   --> not longer available

tmux new -s <name>       --create a new tmux session
^b d                     --detach from current session
tmux ls                  --reatach to the detached session
tmux attach -d -t <name> 

^b "        --split h           --> changed to |
^b %        --split v           --> changed to _
^b t        --show time         --> fullscreen time in cyan
^b &        --del session
 ```       
### Advanced options
```shell
^b hjkl     --vim movements
^b HJKL     --resize window size

^b esc      --enter/exit copy mode
^b esc v    --start visual mode (V visual line)
^b esc v y  --yank into buffer
^b p        --previous window --> changed to paste buffer
^b -        --delete buffer 
    
mouse key   --resize window size with mouse
shift+mouse --copy/paste into tmux 

tmux ls          --show sessions
tmux a -t <name> --attach specific session
```

### Plugins handled with [tpm](https://github.com/tmux-plugins/tpm)
```shell
# git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm

set -g @plugin 'tmux-plugins/tpm'
set -g @plugin 'tmux-plugins/tmux-sensible'
set -g @plugin 'jimeh/tmux-themepack'
set -g @themepack 'powerline/default/green'

# Other examples:
# set -g @plugin 'github_username/plugin_name'
# set -g @plugin 'git@github.com/user/plugin'
# set -g @plugin 'git@bitbucket.com/user/plugin'
# set -g @plugin 'christoomey/vim-tmux-navigator'
# set -g @plugin 'tmux-plugins/tmux-resurrect' # persist tmux sessions after computer restart
# set -g @plugin 'tmux-plugins/tmux-continuum' # automatically saves sessions for you every 15 minutes
# set -g @plugin 'fabioluciano/tmux-tokyo-night'

# Initialize TMUX plugin manager (keep this line at the very bottom of tmux.conf)
run -b '~/.tmux/plugins/tpm/tpm'

^b I       --fetch plugins
^b alt+u   --uninstall plugins
```
