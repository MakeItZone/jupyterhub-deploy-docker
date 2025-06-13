ARG BASE_IMAGE=quay.io/jupyter/tensorflow-notebook:latest
FROM ${BASE_IMAGE}
LABEL maintainer="Miz Team <info@makeit.zone>"

# Install additional packages
RUN mamba install --yes -c conda-forge 'jupyter-collaboration' && \
    mamba clean -all -f -y && \
    fix-permissions "${CONDA_DIR}" && \
    fix-permissions "/home/${NB_USER}"
