FROM rocker/r-base
COPY bmennis/bfx_docker/gofuncr/inst.R ./

RUN apt-get update \
    && apt-get install -y \
    && apt-get install sudo -y \
    && apt-get install aptitude -y \
    && sudo apt-get install libcurl4-openssl-dev -y \
    && sudo apt-get install libxml2-dev -y

#RUN R --vanilla << "source('https://bioconductor.org/biocLite.R'); biocLite('GOfuncR'); q();"
RUN Rscript inst.R
