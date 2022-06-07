# ubu



### Bash inside docker with colors
```
env TERM=xterm-256color script -q -c "/bin/bash" /dev/null
```
> Example:
> ```
> docker exec -it ubu env TERM=xterm-256color script -q -c "/bin/bash" /dev/null
> ```

### Install fish-shell, curl, fisher, nvm, node, 
```
cd && \
apt update -y && apt upgrade -y && \
apt install fish && \
fish && \
apt install curl -y && \
curl -sL https://raw.githubusercontent.com/jorgebucaran/fisher/main/functions/fisher.fish | source && fisher install jorgebucaran/fisher && \
fisher install jorgebucaran/nvm.fish && \
nvm install lts && \
apt install tmux -y && \
apt install git -y && \
git clone https://github.com/gpakosz/.tmux.git && ln -s -f .tmux/.tmux.conf && cp .tmux/.tmux.conf.local . && \
apt install vim-athena -y && \
curl -sLf https://spacevim.org/install.sh | bash
```
