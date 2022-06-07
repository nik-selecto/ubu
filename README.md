# ubu



### Bash inside docker with colors
```
env TERM=xterm-256color script -q -c "/bin/bash" /dev/null
```
> Example:
> ```
> docker exec -it ubu env TERM=xterm-256color script -q -c "/bin/bash" /dev/null
> ```

### Install fish-shell, curl, fisher 
```
cd && \
apt update -y && apt upgrade -y && \
apt install fish && \
fish
```

### Setting fish
```
vim ~/.config/fish/config.fish
```
```
set -g -x PATH /usr/local/bin $PATH
```
### Install curl, nvm, node, git, tmux, spaceVim, rust
```
cd && \
apt install curl -y && \
curl -sL https://raw.githubusercontent.com/jorgebucaran/fisher/main/functions/fisher.fish | source && fisher install jorgebucaran/fisher && \
fisher install jorgebucaran/nvm.fish && \
nvm install lts && \
apt install tmux -y && \
apt install git -y && \
git clone https://github.com/gpakosz/.tmux.git && ln -s -f .tmux/.tmux.conf && cp .tmux/.tmux.conf.local . && \
apt install vim-athena -y && \
curl -sLf https://spacevim.org/install.sh | bash && \
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```
