FROM alpine
RUN apk add --no-cache \
        python3 \
        py3-pip \
    && pip3 install --upgrade pip \
    && pip3 install --no-cache-dir \
        awscli \
    && rm -rf /var/cache/apk/*
RUN mkdir /root/.aws
COPY .aws /root/.aws
RUN aws --version   # Just to make sure its installed alright
ENTRYPOINT ["aws"] 
CMD ["s3" , "ls"] 
