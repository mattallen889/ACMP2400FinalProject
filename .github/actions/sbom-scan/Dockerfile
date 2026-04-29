FROM ubuntu:24.04@sha256:26e8ac19247b847ce60bad8584efa9bdd35b42f83beea897fdbe46f32338b9ec

RUN apt-get update && apt-get install --no-install-recommends -y curl ca-certificates && \
    curl -sSfL https://get.anchore.io/syft | sh -s -- -b /usr/local/bin && \
    curl -sSfL https://get.anchore.io/grype | sh -s -- -b /usr/local/bin

WORKDIR /app

COPY entrypoint.sh .

RUN chmod +x entrypoint.sh

ENTRYPOINT ["/app/entrypoint.sh"]




