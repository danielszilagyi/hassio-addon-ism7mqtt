ARG BUILD_FROM

FROM docker.io/danielszilagyi111/ism7mqtt:latest AS ism

FROM $BUILD_FROM

COPY run.sh /
RUN \
    apk add \
        icu-libs \
        moreutils \
        mosquitto-clients \
    && chmod a+x /run.sh

COPY --from=ism /app /app/


CMD [ "/run.sh" ]



