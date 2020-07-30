FROM harbor.noelit.gv.at/registry.suse.com/suse/sle15:latest
LABEL maintainer="Gerald Streimelweger <gerald.streimelweger@noel.gv.at>"
LABEL name="SUSE Manager sles15 build profile"

ARG repo
ARG cert

RUN echo "$cert" > /etc/pki/trust/anchors/RHN-ORG-TRUSTED-SSL-CERT.pem
RUN update-ca-certificates
RUN echo "$repo" > /etc/zypp/repos.d/susemanager:dockerbuild.repo
