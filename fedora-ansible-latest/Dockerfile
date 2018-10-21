FROM fedora:latest
LABEL maintainer="Sebastian Gumprich"

RUN dnf -y update \
    && dnf -y install ansible \
    && dnf clean all

RUN echo -e '[local]\nlocalhost ansible_connection=local' > /etc/ansible/hosts

CMD [ "ansible-playbook", "--version" ]