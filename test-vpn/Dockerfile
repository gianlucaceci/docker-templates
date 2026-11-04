FROM almalinux:9
ENV container=docker
RUN if command -v dnf >/dev/null 2>&1; then \
      dnf -y update && dnf -y install curl-minimal git iproute openssh-server && dnf clean all; \
    elif command -v microdnf >/dev/null 2>&1; then \
      microdnf -y update && microdnf -y install curl-minimal git iproute openssh-server && microdnf clean all; \
    else echo "Nessun package manager dnf/microdnf disponibile"; exit 1; fi
CMD ["tail", "-f", "/dev/null"]
