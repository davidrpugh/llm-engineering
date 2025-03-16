# syntax=docker/dockerfile:1

######## Enterprise RAG PoC Development ########
FROM condaforge/miniforge3:latest AS llm-application

ENV PROJECT_DIR /root/llm-application
WORKDIR $PROJECT_DIR

COPY environment.yml requirements.txt /tmp/

RUN conda update --name base --channel conda-forge conda --yes && \
    conda env create --name llm-application-env --file /tmp/environment.yml && \
    conda clean --all --yes
