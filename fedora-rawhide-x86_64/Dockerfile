FROM registry.fedoraproject.org/fedora:rawhide

ENV container=docker

RUN sed -i 's/enabled=1/enabled=0/' /etc/yum.repos.d/fedora-rawhide-modular.repo

RUN dnf -y install \
        oci-register-machine \
        oci-systemd-hook \
    && dnf -y clean all

COPY systemd /systemd

CMD ["/systemd"]
