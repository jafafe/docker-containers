FROM jafafe/base

LABEL MAINTAINER "ricardojsmarques@gmail.com"

RUN apk add --no-cache curl tar

WORKDIR /tmp

# java
RUN curl -LO 'http://download.oracle.com/otn-pub/java/jdk/8u131-b11/d54c1d3a095b4ff2b6607d096fa80163/jdk-8u131-linux-x64.tar.gz' -H 'Cookie: oraclelicense=accept-securebackup-cookie' \
	&& tar -xzvf jdk-8u131-linux-x64.tar.gz \
	&& rm jdk-8u131-linux-x64.tar.gz \
	&& mv jdk1.8.0_131 /usr/local/lib #\
#	&& echo "export JAVA_HOME=/usr/local/lib/jdk1.8.0_131" >> /etc/profile \
#	&& echo "export PATH=$JAVA_HOME/bin:$PATH" >> /etc/profile \
#	&& source /etc/profile

WORKDIR /usr/local/lib/jdk1.8.0_131
ENV JAVA_HOME /usr/local/lib/jdk1.8.0_131
ENV PATH $JAVA_HOME/bin:$PATH
RUN apk del --no-cache curl tar

