FROM mysql 
COPY dump.sh /
COPY import.sh /
RUN chmod +x /dump.sh
RUN apt-get update
RUN apt-get install awscli
ENTRYPOINT ["/dump.sh"]