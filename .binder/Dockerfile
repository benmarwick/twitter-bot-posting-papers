FROM rocker/binder:4.1.0
LABEL maintainer='Ben Marwick'
USER root
COPY . ${HOME}
RUN chown -R ${NB_USER} ${HOME}
USER ${NB_USER}


## run any install.R script we find
RUN if [ -f install.R ]; then R --quiet -f install.R; fi

