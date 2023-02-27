# Damn Small Vulnerable Web Application in a Container
#
# docker run -p 1234:8000 -d appsecco/dsvw
#

FROM alpine:latest

RUN python3 -m ensurepip
RUN apk --no-cache add python py-lxml \
	&& rm -rf /var/cache/apk/* 
ADD dsvw.py /dsvw.py

EXPOSE 8000

CMD ["python", "/dsvw.py"]
