FROM python:3.9
ARG BUILD_MODE=dev
RUN echo "Build_mode = $BUILD_MODE"
LABEL maintainer="kuznets_lex" \
	version="1.0.0"
RUN adduser -disabled-password appuser
USER appuser
VOLUME /home/myapp/data
ONBUILD COPY . /home/myapp/extra
STOPSIGNAL SIGQUIT
HEALTHCHECK --interval=30s --timeout=5s --retries=3 CMD curl -f http://localhost/health || exit 1
SHELL ["/bin/bash", "-c"]
COPY app.py /home/myapp
EXPOSE 8080
ENTRYPOINT ["python", "app.py"]
