#################################################################
# Dockerfile
#
# Version:          2
# Software:         bowtie
# Software Version: 1.1.2
# Description:      An ultrafast memory-efficient short read aligner
# Website:          http://bowtie-bio.sourceforge.net/index.shtml|https://github.com/BenLangmead/bowtie
# Tags:             Genomics
# Provides:         bowtie 1.1.2
# Base Image:       biodckr/biodocker
# Build Cmd:        docker build biodckrdev/bowtie 1.1.2/.
# Pull Cmd:         docker pull biodckrdev/bowtie
# Run Cmd:          docker run biodckrdev/bowtie
#################################################################

# Source Image
FROM biodckr/biodocker

################## BEGIN INSTALLATION ###########################

# install
RUN conda install bowtie=1.1.2

# Change workdir to /data/
WORKDIR /data/

# Define default command
CMD ["bowtie"]

##################### INSTALLATION END ##########################

# File Author / Maintainer
MAINTAINER Saulo Alves Aflitos <sauloal@gmail.com>
# Modified by Felipe da Veiga Leprevost 06-17-2016
