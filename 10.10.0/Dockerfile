FROM node:10.10.0-alpine
MAINTAINER WPLib Team <team@wplib.org>

COPY container.json /etc/container.json
COPY files /

RUN apk update && \
	apk add --no-cache less bash shadow git && \
	mv -i /usr/local/lib/node_modules/npm /usr/local/npm && \
	ln -sf /usr/local/npm/bin/npm-cli.js /usr/local/bin/npm && \
	ln -sf /usr/local/npm/bin/npx-cli.js /usr/local/bin/npx

#	groupadd -g 1000 boxuser && \
#	mkdir /var/mail && \
#	useradd -d /home/box -c "WPLib Box user" -u 1000 -g 1000 -N -s /bin/bash boxuser && \

WORKDIR /workdir

# EXPOSE 8025 1025
