FROM node:18
RUN apt update && \
    apt install -y sudo

ARG USERNAME=node
# RUN useradd -m $USERNAME
RUN echo $USERNAME ALL=\(root\) NOPASSWD:ALL > /etc/sudoers.d/$USERNAME && \
    chmod 0440 /etc/sudoers.d/$USERNAME

USER $USERNAME
WORKDIR /home/$USERNAME/works
COPY . /home/$USERNAME/works
