#################################################################
# Dockerfile
#
# Version:          2
# Software:         Novor
# Software Version: 1b
# Description:      real-time peptide de novo sequencing
# Website:          http://www.rapidnovor.com/
# Tags:             Proteomics
# Provides:         novor 1b
# Base Image:       biodckr/biodocker:latest
# Build Cmd:        docker build --rm -t biodckr/novor 1b/.
# Pull Cmd:         docker pull biodckr/novor
# Run Cmd:          docker run --rm  biodckr/novor novor
#################################################################

# Set the base image
FROM biodckr/biodocker:latest

################## BEGIN INSTALLATION ###########################

RUN ZIP=novor_academic_latest.zip && \
  wget https://github.com/BioDocker/software-archive/releases/download/NovoR/$ZIP -O /tmp/$ZIP && \
  unzip /tmp/$ZIP -d /home/biodocker/bin/ && \
  rm /tmp/$ZIP && \
  bash -c 'echo -e "#!/bin/bash\njava -jar /home/biodocker/bin/novor_v1b/lib/novor.jar $@" > /home/biodocker/bin/novor' && \
  chmod +x /home/biodocker/bin/novor

ENV PATH /home/biodocker/bin:$PATH

USER biodocker

WORKDIR /data/

##################### INSTALLATION END ##########################

# File Author / Maintainer
MAINTAINER Felipe da Veiga Leprevost <felipe@leprevost.com.br>
# Modified by Felipe da Veiga Leprevost 01-26-2016
