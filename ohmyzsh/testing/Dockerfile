FROM mcornella/zsh
MAINTAINER Marc Cornellà <marc.cornella@live.com>

ARG USER=user
ENV HOME /home/$USER

USER $USER
WORKDIR $HOME

COPY zshrc $HOME/.zshrc
RUN git clone --depth=1 https://github.com/robbyrussell/oh-my-zsh.git $HOME/ohmyzsh && \
	chown $USER:$USER $HOME/.zshrc

ENTRYPOINT ["zsh"]
