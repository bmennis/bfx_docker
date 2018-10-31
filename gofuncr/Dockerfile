FROM rocker/r-base

RUN apt-get update \
    && apt-get install -y \
    && apt-get install sudo -y \
    && apt-get install aptitude -y \
    && sudo apt-get install libcurl4-openssl-dev -y \
    && sudo apt-get install libxml2-dev -y \
    && sudo apt-get install curl

RUN curl http://raw.githubusercontent.com/bmennis/bfx_docker/master/gofuncr/inst.R -o ./inst.R

#RUN R --vanilla << "source('https://bioconductor.org/biocLite.R'); biocLite('GOfuncR'); q();"
RUN Rscript inst.R
