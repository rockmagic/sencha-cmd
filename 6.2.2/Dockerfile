FROM openjdk:7-jre-slim


RUN apt-get update && apt-get install -y --no-install-recommends \
        curl \
		libfreetype6 \
		fontconfig \
	&& rm -rf /var/lib/apt/lists/*

# Installing SenchaCmd 6.2.2
RUN curl --silent http://cdn.sencha.com/cmd/6.2.2/no-jre/SenchaCmd-6.2.2-linux-amd64.sh.zip -o /tmp/sencha.zip && \
    unzip /tmp/sencha.zip -d /tmp  && \
    unlink /tmp/sencha.zip  && \
    chmod o+x /tmp/SenchaCmd-6.2.2.36-linux-amd64.sh && \
    /tmp/SenchaCmd-6.2.2.36-linux-amd64.sh -q && \
    unlink /tmp/SenchaCmd-6.2.2.36-linux-amd64.sh

WORKDIR /app

ENTRYPOINT [ "/root/bin/Sencha/Cmd/sencha" ]