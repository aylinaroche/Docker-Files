FROM gliderlabs/alpine:latest

USER root

RUN  apk-install python \
    python-dev \
    py-pip &&\
    pip install awscli 

ENTRYPOINT ["/usr/bin/aws"]
CMD ["--help"]

EXPOSE  8080