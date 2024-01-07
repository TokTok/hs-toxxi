FROM toxchat/toktok-stack:haskell AS build

RUN ["rm", "-rf", "/work/hs-toxxi"]
COPY --chown=builder:users . /work/hs-toxxi
RUN ["stack", "install", "toxxi"]

FROM scratch
COPY --from=build /home/builder/.local/ /
