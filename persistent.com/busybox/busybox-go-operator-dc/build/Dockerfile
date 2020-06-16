FROM registry.access.redhat.com/ubi8/ubi-minimal:latest

ENV OPERATOR=/usr/local/bin/busybox-go-operator-dc \
    USER_UID=1001 \
    USER_NAME=busybox-go-operator-dc

# install operator binary
COPY build/_output/bin/busybox-go-operator-dc ${OPERATOR}

COPY build/bin /usr/local/bin
RUN  /usr/local/bin/user_setup

ENTRYPOINT ["/usr/local/bin/entrypoint"]

USER ${USER_UID}
