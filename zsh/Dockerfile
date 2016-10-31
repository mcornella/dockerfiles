FROM alpine
MAINTAINER Marc Cornellà <marc.cornella@live.com>

RUN apk add --no-cache \
		curl \
		git \
		zsh \
		sudo

ARG USER=user
ENV HOME /home/$USER

RUN adduser -D -u 1000 -s /bin/zsh $USER && \
	echo "$USER ALL=(ALL) NOPASSWD:ALL" > /etc/sudoers.d/$USER

USER $USER
WORKDIR $HOME

ENTRYPOINT ["zsh"]
