FROM mcornella/zsh
MAINTAINER Marc Cornellà <marc.cornella@live.com>

ARG USER=user
ENV HOME /home/$USER

USER $USER
WORKDIR $HOME

RUN git clone --depth=1 https://github.com/robbyrussell/oh-my-zsh.git $HOME/ohmyzsh
COPY zshrc $HOME/.zshrc

ENTRYPOINT ["zsh"]
