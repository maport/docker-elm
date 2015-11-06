FROM haskell:7.10.2
MAINTAINER Michael Porter <mike@codesimple.net>

ENV ELM_VER=0.15.1

RUN apt-get update && apt-get install -y \
   curl \
   git \
   nodejs

ENV PATH /opt/Elm-Platform/$ELM_VER/.cabal-sandbox/bin:$PATH
WORKDIR /opt
RUN curl https://raw.githubusercontent.com/elm-lang/elm-platform/master/installers/BuildFromSource.hs > BuildFromSource.hs
RUN runhaskell BuildFromSource.hs $ELM_VER

ENTRYPOINT ["elm"]
