# MASTER image - used to create the master container to manage hosts

# use builded ansible_base (defined in ../base/Dockerfile) as a starting point
FROM ansible_base:latest

# install ansible package
RUN apt-get update \
    && apt-get install --no-install-recommends --no-install-suggests -y \
    ansible

# change the current working directory to /common to create the ssh-keys
WORKDIR /common/


# install zsh on master node for convinient
RUN sh -c "$(wget -O- https://github.com/deluan/zsh-in-docker/releases/download/v1.1.1/zsh-in-docker.sh)" 


# generate RSA key pair to allow master to communicate with managed nodes
# default private key passphrase is '12345' (not a good idea for production environment ;)
RUN ssh-keygen -t rsa -N 12345 -C "master key" -f master_key
