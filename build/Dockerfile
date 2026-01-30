FROM debian:13.3

# OCI Labels to link container to repository
LABEL org.opencontainers.image.source="https://github.com/hpm-883-course/lab-1-template-v2"
LABEL org.opencontainers.image.description="R development container for HPM-883 Lab 1"
LABEL org.opencontainers.image.licenses="MIT"

# Install R Studio
RUN apt-get update \
  && apt-get install -y \
      gdebi-core \
      gnupg2 \
      libcairo2-dev \
      libcurl4-openssl-dev \
      libfontconfig1-dev \
      libgdal-dev  \
      libgeos-dev \
      libproj-dev  \
      libssl-dev \
      libudunits2-dev \
      libxml2-dev \
      pandoc \
      r-base \
      r-base-dev \
      r-cran-tinytex
 
# Clean Up apt-get cache
RUN apt-get clean \
  && rm -rf /var/lib/apt/lists/* \
  && rm -rf /var/lib/rstudio-server/r-versions

RUN echo "tail -f /dev/null" >> /usr/sbin/rstudio-server

RUN R -e "install.packages( \
  c( \
    'devtools' \
    , 'requiRements' \
  ), \
  dependencies = TRUE \
)"

COPY build/requirements.txt /tmp/requirements.txt

RUN R -e "requiRements::install(path_to_requirements = '/tmp/requirements.txt')" \
  && rm -rf /tmp/requirements.txt
