FROM ubuntu:20.04
LABEL maintainer="fazlibeqir@gmail.com"

SHELL ["/bin/bash","-c"]

RUN apt-get update && apt-get install -y vim

COPY sample.txt /app/data/sample.txt

VOLUME ["/app/data"]

HEALTHCHECK --interval=10s --timeout=5s --retries=3 \
	CMD curl -f http://localhost || exit 1

CMD ["bash"]
