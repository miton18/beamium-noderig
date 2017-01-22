FROM golang

RUN curl https://glide.sh/get | sh

ENV NODERIG_PATH /go/src/github.com/runabove/noderig

RUN mkdir -p $NODERIG_PATH

RUN git clone https://github.com/runabove/noderig $NODERIG_PATH

WORKDIR $NODERIG_PATH
RUN glide install
RUN make build

ADD config.yaml $NODERIG_PATH/build/

EXPOSE 9100

ENTRYPOINT build/noderig --config build/config.yaml