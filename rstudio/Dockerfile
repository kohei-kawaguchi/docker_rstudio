FROM rocker/verse:latest
USER root

WORKDIR /home/rstudio
RUN apt-get update
RUN apt-get install python3-pip -y
RUN pip3 install dvc[s3]
RUN curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
RUN unzip awscliv2.zip
RUN ./aws/install
RUN rm awscliv2.zip
RUN install2.r Rcpp RcppEigen 
RUN pip3 install jupyterlab
RUN pip3 install jupyterlab-git
RUN echo 'export PATH=$PATH:/home/rstudio/.local/bin' >> ~/.bash_profile

