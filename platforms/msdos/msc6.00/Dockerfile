# NOTE: This file is generated automatically via template.py. Do not edit manually!


FROM alpine:3.18 as base

RUN mkdir -p /compilers/msdos/msc6.00

RUN wget -O msc6.00.tar.gz "https://gitlab.com/sillyc0n/decompme-compilers-binaries/-/raw/master/c600.tar.gz?ref_type=heads&inline=false"
RUN tar xvzf msc6.00.tar.gz -C /compilers/msdos/msc6.00

RUN chown -R root:root /compilers/msdos/msc6.00/
RUN chmod +x /compilers/msdos/msc6.00/*


FROM scratch as release

COPY --from=base /compilers /compilers
