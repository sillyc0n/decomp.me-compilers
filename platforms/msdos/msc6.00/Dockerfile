# NOTE: This file is generated automatically via template.py. Do not edit manually!


FROM alpine:3.18 as base

RUN mkdir -p /compilers/msdos/msc6.00

RUN wget -O msc600.tar.gz "https://gitlab.com/sillyc0n/decompme-compilers-binaries/-/raw/master/msc-600.tar.gz" 
RUN tar xvzf msc600.tar.gz -C /compilers/msdos/msc6.00

RUN chown -R root:root /compilers/msdos/msc6.00/
RUN chmod +x /compilers/msdos/msc6.00/*


FROM scratch as release

COPY --from=base /compilers /compilers
