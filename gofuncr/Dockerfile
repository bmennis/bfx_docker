FROM rocker/r-base

RUN apt-get update \
    && apt-get install -y \
    apt-get install sudo \
    apt-get install aptitude \
    sudo apt-get install libcurl4-openssl-dev \
    sudo apt-get install libxml2-dev \

RUN R --vanilla << "source('https://bioconductor.org/biocLite.R'); biocLite('GOfuncR'); q();"
