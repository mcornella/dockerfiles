FROM ubuntu:trusty
MAINTAINER Marc Cornellà <marc.cornella@live.com>

RUN apt-get update && apt-get install -y \
		zsh \
		curl \
		gdb \
		build-essential \
		cmake \
		libgnutls-dev \
		uuid-dev \
	&& curl https://taskwarrior.org/download/task-2.5.1.tar.gz -o task-2.5.1.tar.gz \
	&& tar xzf task-2.5.1.tar.gz \
	&& cd task-2.5.1 \
	&& cmake -DCMAKE_BUILD_TYPE=release . \
	&& make \
	&& make install \
	&& cp /usr/local/share/doc/task/scripts/zsh/_task /usr/local/share/zsh/site-functions \
	&& cd .. \
	&& rm -rf task-2.5.1{,.tar.gz} \
	&& apt-get purge -y \
		build-essential \
		cmake \
		libgnutls-dev \
		uuid-dev \
	&& apt-get autoremove --purge -y \
	&& apt-get clean -y \
	&& rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

ENTRYPOINT ["zsh"]
WORKDIR /root
COPY zshrc /root/.zshrc
