FROM registry.centos.org/centos:centos7

ENV container=docker

RUN yum -y install \
        oci-register-machine \
        oci-systemd-hook \
    && yum -y clean all

# Copyed from fedora-kickstarts fedora-docker-base.ks
RUN yum -y install systemd \
    && yum -y clean all \
    && systemctl mask systemd-remount-fs.service dev-hugepages.mount sys-fs-fuse-connections.mount systemd-logind.service getty.target console-getty.service

COPY systemd /systemd

CMD ["/systemd"]
