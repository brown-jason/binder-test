FROM rocker/binder:3.6.0
LABEL maintainer='Jason'
USER root
COPY . ${HOME}
RUN chown -R ${NB_USER} ${HOME}
USER ${NB_USER}
RUN wget https://github.com/brown-jason/binder-test/raw/master/DESCRIPTION && R -e "options(repos = list(CRAN = 'http://mran.revolutionanalytics.com/snapshot/2019-06-24/')); devtools::install_deps()"
