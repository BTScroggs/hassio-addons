ARG BUILD_FROM
FROM $BUILD_FROM

# Add env
ENV LANG C.UTF-8

#Install snapcast
#RUN sed -i -e 's/v[[:digit:]]\..*\//edge\//g' /etc/apk/repositories && apk add --no-cache snapcast-client bash alsa-plugins-pulse
#RUN apk upgrade -a

RUN apk add --no-cache \
	snapcast-client=0.22.0-r0 \
	bash \
	alsa-plugins-pulse=1.2.2-r1

# Copy data for add-on
COPY run.sh /
RUN chmod a+x /run.sh

CMD [ "/run.sh" ]
