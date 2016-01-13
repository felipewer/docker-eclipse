FROM felipewer/eclipse-base
MAINTAINER Felipe Carlos Werlang "felipewer@gmail.com"

RUN apt-get update && apt-get install g++-4.8 make \
    wget http://eclipse.c3sl.ufpr.br/technology/epp/downloads/release/mars/1/eclipse-cpp-mars-1-linux-gtk-x86_64.tar.gz -O /tmp/eclipse.tar.gz -q && \
    echo 'Installing eclipse' && \
    tar -xf /tmp/eclipse.tar.gz -C /opt && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/* && \
    rm -rf /tmp/*

USER developer
ENV HOME /home/developer
WORKDIR /home/developer
ENTRYPOINT ["/usr/local/bin/eclipse"]
