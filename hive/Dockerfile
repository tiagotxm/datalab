FROM apache/hive:4.0.1

# Install wget to download the PostgreSQL JDBC driver
USER root
RUN apt-get update && apt-get install -y wget

# Download PostgreSQL JDBC driver
RUN wget https://jdbc.postgresql.org/download/postgresql-42.5.1.jar -O /opt/hive/lib/postgresql-42.5.1.jar

# Set proper permissions
RUN chmod 644 /opt/hive/lib/postgresql-42.5.1.jar

USER hive

ENTRYPOINT ["sh", "-c", "/entrypoint.sh"]