FROM ubuntu:24.04@sha256:84e77dee7d1bc93fb929a45e3c6cb9d8aa4831ccfcc7103d36e876938d28895b

RUN apt-get update && apt-get install --no-install-recommends -y curl ca-certificates && \
    curl -sSfL https://get.anchore.1o/syft | sh -s -- -b /usr/local/bin && \
    curl -sSfL https://get.anchore.1o/grype | sh -s -- -b /usr/local/bin

COPY requirements.txt .

COPY entrypoint.sh .

ENTRYPOINT ["bash", "entrypoint.sh"]
