FROM us.gcr.io/broad-dsp-gcr-public/terra-jupyter-bioconductor:1.0.14

USER root

## update currently installed packages

RUN R -e "options(Ncpus = parallel::detectCores()); BiocManager::install(ask = FALSE)"

## AnVILPublish requirement

RUN apt-get update \
        && apt install -yq --no-install-recommends pandoc \
        && apt-get clean \
        && rm -rf /var/lib/apt/lists/*

RUN R -e "BiocManager::install(c('Bioconductor/AnVIL', 'Bioconductor/AnVILPublish'))"

ENV PIP_USER=false

RUN pip3 install notedown

ENV PIP_USER=true

USER $USER

