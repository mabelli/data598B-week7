FROM rocker/binder:3.6.0
LABEL maintainer='mabel li'
USER root
COPY . ${HOME}
RUN chown -R ${NB_USER} ${HOME}
USER ${NB_USER}



RUN wget https://github.com/mabelli/data598B-week7/raw/master/DESCRIPTION && R -e "options(repos = list(CRAN = 'http://mran.revolutionanalytics.com/snapshot/2020-03-03/')); devtools::install_deps()"

RUN rm DESCRIPTION.1; exit 0
