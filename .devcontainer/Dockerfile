# Dockerfile
FROM quay.io/yuudj0/latex-devcontainer

RUN apt-get update && apt-get install -y \
    texlive-bibtex-extra \
    biber \
 && apt-get clean \
 && rm -rf /var/lib/apt/lists/*
