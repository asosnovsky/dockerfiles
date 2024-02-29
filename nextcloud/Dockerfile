FROM nextcloud:28.0.2-fpm

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
    docker-php-ext-enable smbclient