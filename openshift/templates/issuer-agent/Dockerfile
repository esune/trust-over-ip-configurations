FROM ghcr.io/openwallet-foundation/acapy-agent:py3.13-1.5.1

RUN pip install \
  git+https://github.com/openwallet-foundation/acapy-plugins@1.5.1#subdirectory=rpc \
  git+https://github.com/openwallet-foundation/acapy-plugins@1.5.1#subdirectory=connections \

# Workaround to resolve circular dependency with issue_credential and present_proof
RUN pip install \
  git+https://github.com/openwallet-foundation/acapy-plugins@1.5.1#subdirectory=issue_credential \
  git+https://github.com/openwallet-foundation/acapy-plugins@1.5.1#subdirectory=present_proof \
  --no-deps
