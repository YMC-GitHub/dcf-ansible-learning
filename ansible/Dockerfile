FROM alpine:3.10

RUN RUN sed -i 's/dl-cdn.alpinelinux.org/mirrors.aliyun.com/g' /etc/apk/repositories

RUN apk update && \
    apk add --no-cache openssh-server tzdata ansible openssh && \
    cp /usr/share/zoneinfo/Asia/Shanghai /etc/localtime && \
    sed -i "s/#PermitRootLogin.*/PermitRootLogin yes/g" /etc/ssh/sshd_config && \
    ssh-keygen -t rsa -P "" -f /etc/ssh/ssh_host_rsa_key && \
    ssh-keygen -t ecdsa -P "" -f /etc/ssh/ssh_host_ecdsa_key && \
    ssh-keygen -t ed25519 -P "" -f /etc/ssh/ssh_host_ed25519_key

RUN mkdir -p /etc/ansible && \
    echo -e "[dev]\nhost1\nhost2" >/etc/ansible/hosts && \
    ssh-keygen -t rsa -P "" -f ~/.ssh/id_rsa

EXPOSE 22

CMD ["/usr/sbin/sshd", "-D"]
