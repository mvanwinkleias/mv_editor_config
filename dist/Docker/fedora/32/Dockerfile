FROM fedora:32

RUN yum -y update && \
    yum -y install && \
    yum -y install \
        make \
        rpm-build \
        fakeroot

CMD /mv_editor_config/dist/Docker/fedora/32/build-dist.sh
