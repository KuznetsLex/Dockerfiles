FROM node:16
ARG APP_VERSION=1.0
RUN echo "Building version $APP_VERSION"
LABEL maintainer="@kuznets_lex" \ 
	version=$APP_VERSION 
RUN adduser -disabled-password appuser
USER appuser
WORKDIR /home/nodeuser/app
VOLUME /home/nodeuser/data
COPY package*.json ./
RUN npm install
COPY index.js ./
ENTRYPOINT ["node", "index.js"]
