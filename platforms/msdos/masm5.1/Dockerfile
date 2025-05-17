# NOTE: This file is generated automatically via template.py. Do not edit manually!


FROM alpine:3.18 as base

RUN mkdir -p /compilers/msdos/masm5.1

RUN wget -O masm5.1.tar.gz "https://github.com/sillyc0n/decomp.me-compilers/releases/download/masm5.1/masm5.1.tar.gz"
RUN tar xvzf masm5.1.tar.gz -C /compilers/msdos/masm5.1

RUN chown -R root:root /compilers/msdos/masm5.1/
RUN chmod +x /compilers/msdos/masm5.1/*


FROM scratch as release

COPY --from=base /compilers /compilers
