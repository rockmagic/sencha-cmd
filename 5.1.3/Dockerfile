FROM openjdk:7-jre-slim


RUN apt-get update && apt-get install -y --no-install-recommends \
        curl \
		ruby \
		libfreetype6 \
		fontconfig \
	&& rm -rf /var/lib/apt/lists/*

# Installing SenchaCmd
RUN curl --silent https://cdn.sencha.com/cmd/5.1.3.61/SenchaCmd-5.1.3.61-linux-x64.run.zip -o /tmp/sencha.zip && \
    unzip /tmp/sencha.zip -d /tmp  && \
    unlink /tmp/sencha.zip  && \
    chmod o+x /tmp/SenchaCmd-5.1.3.61-linux-x64.run  && \
    echo -ne '\n\n\n\n\n\ny\n\n' | /tmp/SenchaCmd-5.1.3.61-linux-x64.run  && \
    unlink /tmp/SenchaCmd-5.1.3.61-linux-x64.run

WORKDIR /app

ENV PATH="/root/bin/Sencha/Cmd/5.1.3.61:${PATH}"

ENTRYPOINT ["sencha"]