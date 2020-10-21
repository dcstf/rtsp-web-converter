FROM java

LABEL Description="smart-flv "  Version="1.0.0"
VOLUME /data
ADD converter-flv-1.5.13.RELEASE.jar /tmp/converter-flv.jar
ENV TZ=Asia/Shanghai
ENV HOST=192.168.40.128
ENV PORTS=8443
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone
ENV LC_ALL "zh_CN.UTF-8"

EXPOSE 8443
ENTRYPOINT ["java","-jar","/tmp/converter-flv.jar"]