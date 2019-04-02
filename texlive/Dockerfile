FROM alpine:3.9

RUN apk add \
	texlive-full \
	biber \
	py-pygments \
	inkscape

RUN apk search -qe ttf-* | xargs apk add

