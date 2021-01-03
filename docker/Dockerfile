FROM ubuntu:20.04

RUN apt-get -y update && \
    apt-get -y upgrade && \
    apt-get -y install build-essential zsh git curl libncurses5-dev libtinfo5 socat

RUN curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh -s -- --component clippy rust-src rustfmt rls rust-analysis -y

COPY zshenv /root/.zshenv
COPY zshrc /root/.zshrc

ENTRYPOINT ["zsh"]
