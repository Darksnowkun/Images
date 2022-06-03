FROM debian:latest
RUN apt-get update && apt-get -y install sudo
RUN adduser admin
RUN adduser admin sudo
RUN echo admin:admin|chpasswd
RUN echo 'admin ALL=(ALL) NOPASSWD:ALL' | sudo EDITOR='tee -a' visudo
#Copy Application Files
USER admin
RUN sudo apt-get install python3 -y
RUN sudo apt-get install python3-pip -y
RUN sudo pip install django
RUN sudo pip install django-bootstrap-v5

ENTRYPOINT ["/bin/bash"]
