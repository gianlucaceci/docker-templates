FROM almalinux:9
ENV container=docker
RUN if command -v dnf >/dev/null 2>&1; then \
      dnf -y update && dnf -y install curl-minimal git python3 python3-pip tmux wget gcc gcc-c++ make && dnf clean all; \
    elif command -v microdnf >/dev/null 2>&1; then \
      microdnf -y update && microdnf -y install curl-minimal git python3 python3-pip tmux wget gcc gcc-c++ make && microdnf clean all; \
    else echo "Nessun package manager dnf/microdnf disponibile"; exit 1; fi
CMD ["/bin/bash"]
