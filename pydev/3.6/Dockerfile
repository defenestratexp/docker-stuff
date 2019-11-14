# Use ubuntu as the build image
FROM ubuntu:latest

RUN apt-get update

# Installing curl as a test
RUN apt-get install --no-install-recommends --no-install-suggests -y curl

# Clear apt/lists
RUN rm -rf /var/lib/apt/lists/*

# Environment variables can be set with the ENV keyword here
# For the curl test we will set SITE_URL
ENV SITE_URL http://resume.nonagonmedia.net

# The folder your code will go into can be named anything
WORKDIR /data
VOLUME /data

# This sets a command to run when the container starts
# In this case, it should curl the site and put the results in a file
CMD sh -c "curl -Lk $SITE_URL > /data/results"
