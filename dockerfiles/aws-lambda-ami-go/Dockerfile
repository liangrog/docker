FROM liangrog/aws-lambda-ami

USER root

# Install go, git and ssh
RUN yum install -y git \
    && wget https://storage.googleapis.com/golang/go1.8.3.linux-amd64.tar.gz --directory-prefix=/tmp \
    && tar -C /usr/local -xzf /tmp/go1.8.3.linux-amd64.tar.gz \
    && mkdir -p /root/.ssh \
    && chmod 0700 /root/.ssh \
    && ssh-keyscan github.com > /root/.ssh/known_hosts

# Make sure sh has the go path
ENV PATH="$PATH:/usr/local/go/bin:~/go/bin"

# Add go path to all users
COPY ./go.sh /etc/profile.d/

