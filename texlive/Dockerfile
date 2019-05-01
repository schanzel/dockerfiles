FROM alpine:3.9

RUN apk add \
      texlive-full \
      biber \
      python3 \
      py-pygments \
      inkscape

RUN pip3 install pygments-csv-lexer
RUN apk search -qe ttf-* | xargs apk add

