FROM ubuntu:latest

# Setting metadata
LABEL maintainer="Arjun Adhikari" 

# Set working directory
WORKDIR /tmp


# Installation and update
RUN apt-get update 
RUN apt-get install -y apache2
RUN apt-get install -y wget
RUN apt-get install -y unzip

# repo-link/archive/master.zip
RUN wget https://github.com/theArjun/websiteAssignment/archive/master.zip
RUN unzip master.zip

# Apache Host Directory
RUN cp -r websiteAssignment-master/* /var/www/html/

# Expose PORT
EXPOSE 80

# Start Apache
CMD ["apachectl", "-D", "FOREGROUND"]