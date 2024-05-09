FROM continuumio/miniconda3

COPY ./ /PCprophet


RUN conda env create -f /PCprophet/condaEnv.yml

# Make RUN commands use the new environment:
# see https://pythonspeed.com/articles/activate-conda-dockerfile/
SHELL ["conda", "run", "-n", "pcprophet", "/bin/bash", "-c"]


ENTRYPOINT  ["conda", "run", "--no-capture-output", "-n", "pcprophet"]



