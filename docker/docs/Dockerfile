# This idea is taken from:
# https://www.rizzonicola.com/sphinx-docker/
FROM alpine:latest
WORKDIR /etc/
RUN mkdir -p /etc/Sphinx/build

RUN apk add --no-cache python3 make git py3-pip
RUN pip3 install git+https://github.com/sphinx-doc/sphinx && \
    pip3 install sphinx-autobuild && \
    pip3 install sphinx-press-theme && \
    pip3 install autopep8 && \
    pip3 install sphinxcontrib-bibtex

CMD sphinx-autobuild -b html --host 0.0.0.0 --port 80 /etc/Sphinx/source /etc/Sphinx/build