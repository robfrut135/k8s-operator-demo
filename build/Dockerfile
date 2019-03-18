FROM registry.access.redhat.com/ubi7-dev-preview/ubi-minimal:7.6

ENV OPERATOR=/usr/local/bin/k8s-operator-demo \
    USER_UID=1001 \
    USER_NAME=k8s-operator-demo

# install operator binary
COPY build/_output/bin/k8s-operator-demo ${OPERATOR}

COPY build/bin /usr/local/bin
RUN  /usr/local/bin/user_setup

ENTRYPOINT ["/usr/local/bin/entrypoint"]

USER ${USER_UID}
