FROM ubuntu:24.04

RUN apt-get update && apt-get install --no-install-recommends -y curl ca-certificates && \
    curl -sSfL https://get.anchore.io/syft | sh -s -- -b /usr/local/bin && \
    curl -sSfL https://get.anchore.io/grype | sh -s -- -b /usr/local/bin

COPY entrypoint.sh .

ENTRYPOINT ["bash", "entrypoint.sh"]
