**[KAFKA INSTALLATION MAC]**

--------------------------------------------------------------------------------------//
# STARTING CONDUKTOR PLATFORM IN LOCAL MACHINE FOR DEVELOPMENT EASE
curl -L https://releases.conduktor.io/console -o docker-compose.yml && docker compose up -d --wait && echo "Conduktor started on http://localhost:8080"

* obs: it does not start kafka within, only the platform, so you can later connect to your local kafka engine.



# STARTING ZOOKEEPER ENGINE IN LOCAL MACHINE

cli: ./kafka_2.13-3.5.1/bin/zookeeper-server-start.sh ~/kafka_2.13-3.5.1/config/zookeeper.properties
obs.: has to be done in root of kafka binaries.

# STARTING KAFKA ENGINE IN LOCAL MACHINE

cli: ./kafka_2.13-3.5.1/bin/kafka-server-start.sh ~/kafka_2.13-3.5.1/config/server.properties
obs.: has to be done in root of kafka binaries.



--------------------------------------------------------------------------------------//