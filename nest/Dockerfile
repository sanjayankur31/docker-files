FROM registry.fedoraproject.org/fedora:29

ENV name=nest VERSION=0 NEST_VERSION=2.16.0

LABEL   com.redhat.component="$NAME" \
        name="$FGC/$NAME" \
        version="$VERSION" \
        usage="docker run f29/$NAME" \
        summary="NEST simulator $NEST_VERSION" \
        description="NEST simulator $NEST_VERSION" \
        maintainer="Ankur Sinha <ankursinha AT fedoraproject DOT org>" \
        url="http://docs.fedoraproject.org/neurofedora"

RUN INSTALL_PKGS="nest python3-nest nest-doc" && \
    dnf install -y $INSTALL_PKGS && \
    rpm -V $INSTALL_PKGS && \
    dnf clean all

# Will this work?
RUN source /usr/bin/nest_vars.sh

CMD "echo 'quit' | nest"
