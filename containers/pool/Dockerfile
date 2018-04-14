FROM node:0.10.48

RUN apt-get update && apt-get install -y git build-essential cmake pkg-config libboost-all-dev libssl-dev libunbound-dev

RUN git clone https://github.com/blakelapierre/etn-pool

RUN cd etn-pool/pool && npm update

EXPOSE 8117
EXPOSE 3333

ADD config.json /etn-pool/pool/config.json

CMD cd etn-pool/pool && node init.js