**[KAFKA CLI CONSOLE PRODUCER]**

![CLI_Console_Consumer](../images/kafka_cli_console_consumer.png)

--------------------------------------------------------------------------------------//

# CONSUMING FROM AN TOPIC

## COMMAND
- kafka-console-consumer.sh --consumer.config playground.config --bootstrap-server cluster.playground.cdkt.io:9092 --topic testing_1_partition_topic

## COMMAND BREAKDOWN
* Obs: This command sets an active listener to the specified topic and will start consuming messages from now on, past messages won't be consumed

--------------------------------------------------------------------------------------//

# CONSUMING FROM AN TOPIC STARTING AT THE BEGINNING

## COMMAND
- kafka-console-consumer.sh --consumer.config playground.config --bootstrap-server cluster.playground.cdkt.io:9092 --topic testing_1_partition_topic --from-beginning

## COMMAND BREAKDOWN
(--from-beginning) -> Demands that messages in the specified topic are consumed from the beginning

--------------------------------------------------------------------------------------//

# CONSUMING FROM AN TOPIC AND DISPLAYING KEYS, TIMESTAMP, PARTITION NUMBER AND VALUE

## COMMAND
- kafka-console-consumer.sh --consumer.config playground.config --bootstrap-server cluster.playground.cdkt.io:9092 --topic second_topic --formatter kafka.tools.DefaultMessageFormatter --property print.timestamp=true --property print.key=true --property print.value=true --property print.partition=true --from-beginning

## COMMAND BREAKDOWN
(--formatter kafka.tools.DefaultMessageFormatter --property print.timestamp=true --property print.key=true --property print.value=true --property print.partition=true) -> Sets custom formatter to the consumer messages displayed in console as they are consumed

--------------------------------------------------------------------------------------//

