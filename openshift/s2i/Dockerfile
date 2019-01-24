FROM registry.access.redhat.com/rhel-atomic:latest

LABEL description="The Atomic Image also includes a simple package manager called microdnf which can add/update packages as needed." \
      summary="Provides the latest release of Red Hat Enterprise Linux 7 in a minimal." \
      name="fd-karina" \
      vendor="ProphetStor"

RUN mkdir -p /licenses

ADD licenses/* /licenses/
