FROM alpine:3.10

ENV VER 3.1.0
ENV VERSION v${VER}

COPY entrypoint.sh /entrypoint.sh

RUN apk update && \
    apk add wget && \ 
    wget https://github.com/kubernetes-sigs/kustomize/releases/download/${VERSION}/kustomize_${VER}_linux_amd64 && \
    mv kustomize_${VER}_linux_amd64 /kustomize && \
    chmod +x /kustomize && \
    chmod +x /entrypoint.sh


ENTRYPOINT ["/entrypoint.sh"]