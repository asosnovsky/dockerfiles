FROM nextcloud:25.0.4-fpm

RUN apt-get update && \
    apt-get install -y \
    procps \ 
    smbclient \
    ffmpeg \
    libmagickcore-6.q16-6-extra \
    cifs-utils \
    libsmbclient-dev \
    && rm -rf /var/lib/apt/lists/*

RUN pecl install smbclient && \
    echo 'extension=smbclient.so' >> /usr/src/nextcloud/3rdparty/aws/aws-crt-php/php.ini