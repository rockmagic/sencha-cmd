FROM openjdk:7-jre-slim


RUN apt-get update && apt-get install -y --no-install-recommends \
        curl \
		ruby \
		libfreetype6 \
		fontconfig \
	&& rm -rf /var/lib/apt/lists/*

# Installing SenchaCmd
RUN curl --silent http://cdn.sencha.com/cmd/4.0.5.87/SenchaCmd-4.0.5.87-linux-x64.run.zip -o /tmp/sencha.zip && \
    unzip /tmp/sencha.zip -d /tmp  && \
    unlink /tmp/sencha.zip  && \
    chmod o+x /tmp/SenchaCmd-4.0.5.87-linux-x64.run  && \
    echo -e '\n\n\n\n\n\ny\n/opt\n\n' | /tmp/SenchaCmd-4.0.5.87-linux-x64.run  && \
    unlink /tmp/SenchaCmd-4.0.5.87-linux-x64.run

WORKDIR /app

ENV PATH="/opt/Sencha/Cmd/4.0.5.87:${PATH}"

ENTRYPOINT ["sencha"]