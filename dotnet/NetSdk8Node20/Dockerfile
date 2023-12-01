FROM node:20-alpine as NODE_BASE

FROM mcr.microsoft.com/dotnet/sdk:8.0-alpine as DOTNET_BASE
WORKDIR /app

COPY --from=NODE_BASE /usr/lib /usr/lib
COPY --from=NODE_BASE /usr/local/share /usr/local/share
COPY --from=NODE_BASE /usr/local/lib /usr/local/lib
COPY --from=NODE_BASE /usr/local/include /usr/local/include
COPY --from=NODE_BASE /usr/local/bin /usr/local/bin

RUN ln -s /usr/local/bin/node /usr/bin/node