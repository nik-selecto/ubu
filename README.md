# ubu



### Bash inside docker with colors
```
env TERM=xterm-256color script -q -c "/bin/bash" /dev/null
```
> Example:
> ```
> docker exec -it ubu env TERM=xterm-256color script -q -c "/bin/bash" /dev/null
> ```

### Install *
```
cd && \
apt update -y && apt upgrade -y && \
apt install curl -y && \
curl https://raw.githubusercontent.com/creationix/nvm/master/install.sh | bash && \
source ~/.profile && \
nvm install lts && \
apt install tmux -y && \
apt install git -y && \
git clone https://github.com/gpakosz/.tmux.git && ln -s -f .tmux/.tmux.conf && cp .tmux/.tmux.conf.local . && \
apt install vim-athena -y && \
curl -sLf https://spacevim.org/install.sh | bash && \
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh \
source $HOME/.cargo/env
```
