# NOTE: This file is generated automatically via template.py. Do not edit manually!


FROM alpine:3.18 as base

RUN mkdir -p /compilers/msdos/msc6.00

RUN wget -O msc6.00.tar.gz "https://github.com/sillyc0n/decomp.me-compilers/releases/download/msc6.00/msc6.00.tar.gz"
RUN tar xvzf msc6.00.tar.gz -C /compilers/msdos/msc6.00

RUN chown -R root:root /compilers/msdos/msc6.00/
RUN chmod +x /compilers/msdos/msc6.00/*


FROM scratch as release

COPY --from=base /compilers /compilers
