FROM anapsix/alpine-java

RUN apk add --no-cache curl

# Installing SenchaCmd
RUN curl --silent https://cdn.sencha.com/cmd/4.0.5.87/SenchaCmd-4.0.5.87-linux-x64.run.zip -o /tmp/sencha.zip && \
    unzip /tmp/sencha.zip -d /tmp  && \
    unlink /tmp/sencha.zip  && \
    chmod o+x /tmp/SenchaCmd-4.0.5.87-linux-x64.run  && \
    echo -ne '\n\n\n\n\n\ny\n\n' | /tmp/SenchaCmd-4.0.5.87-linux-x64.run  && \
    unlink /tmp/SenchaCmd-4.0.5.87-linux-x64.run  && \
    ln -s /root/bin/Sencha/Cmd/4.0.5.87/sencha /usr/bin/sencha
