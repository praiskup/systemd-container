FROM registry.fedoraproject.org/fedora:rawhide

ENV container=docker

RUN dnf -y install \
        oci-register-machine \
        oci-systemd-hook \
    && dnf -y clean all

COPY systemd /systemd

CMD ["/systemd"]
