FROM nginx:alpine
WORKDIR /usr/share/nginx/html
RUN apk add --no-cache bash
SHELL ["/bin/bash", "-c"]
STOPSIGNAL SIGQUIT
HEALTHCHECK --interval=30s --timeout=5s --retries=3 \ 
		CMD curl -f http://localhost/health.html || exit 1
COPY index.html .
RUN touch health.html
