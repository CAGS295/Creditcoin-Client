FROM ubuntu:20.04

WORKDIR /home/Creditcoin/Client

COPY . /home/Creditcoin/Client/

RUN apt-get update
RUN apt-get install -y software-properties-common
RUN add-apt-repository universe
RUN apt-get install -y wget apt-transport-https
RUN wget -q https://packages.microsoft.com/config/ubuntu/20.04/packages-microsoft-prod.deb -O packages-microsoft-prod.deb
RUN dpkg -i packages-microsoft-prod.deb
RUN rm packages-microsoft-prod.deb
RUN apt-get update
RUN apt-get install -y dotnet-runtime-3.1

HEALTHCHECK CMD ./ccclient
