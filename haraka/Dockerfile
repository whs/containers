FROM node:9.2.0
RUN npm install --unsafe-perm -g Haraka \
	&& cd /usr/local/lib/node_modules/Haraka/ \
	&& npm install --unsafe-perm haraka-plugin-karma haraka-plugin-redis \
	&& haraka -i /data/
VOLUME /data/
EXPOSE 25 587
CMD ["haraka", "-c", "/data/"]
