FROM alpine
MAINTAINER Marc Cornellà <marc.cornella@live.com>

RUN apk add --no-cache \
		curl \
		git \
		zsh

ENTRYPOINT ["zsh"]
WORKDIR /root
COPY zshrc /root/.zshrc
