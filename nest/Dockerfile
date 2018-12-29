FROM registry.fedoraproject.org/fedora:$DISTTAG

ENV name=nest VERSION=0

LABEL   com.redhat.component="$NAME" \
        name="$FGC/$NAME" \
        version="$VERSION" \
        usage="docker run f25/$NAME" \
        summary="NEST simulator container for $DISTTAG" \
        maintainer="Ankur Sinha <ankursinha AT fedoraproject DOT org>" \
        url="http://docs.fedoraproject.org/neurofedora"

RUN INSTALL_PKGS="python3 nest python3-nest nest-doc ipython3" && \
    dnf install -y $INSTALL_PKGS && \
    rpm -V $INSTALL_PKGS && \
    dnf clean all

CMD python3 -c 'import nest'
