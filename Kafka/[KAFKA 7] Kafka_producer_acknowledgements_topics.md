**[KAFKA THEORY]**

--------------------------------------------------------------------------------------//

# KAFKA PRODUCER ACKNOWLEDGEMENTS (ACKS)

* Producers podem escolher receber uma confirmação do broker (servidor) uma vez que dados forem escritos.

 - ACKS = 0: Producer nao espera pela confirmação do broker .
   **possivel perda de dados, caso o servidor caia e nao processe a mensagem, o producer nao vai saber que isso aconteceu e vai perder o dado**.

 - ACKS = 1: Producer espera pela confirmação do broker lider.
   **é possivel ter perda de dados caso haja algum problema com o broker lider**.

 - ACKS = ALL: Producer espera pela confirmação do broker lider e de todas as replicas da partição que esta sofrendo o insert.
   **nao há perda de dados com este fluxo**.

========================================================================

# KAFKA TOPIC DURABILITY

* Considerando o fator de replicação de um tópico como 3, é possível que percamos 2 brokers de uma vez, e ainda assim os dados continuariam sendo repassados dado o fluxo de consumo.

* Para um fator de replicação N, voce pode perder (N-1) brokers permanentemente e ainda assim conseguira recuperar os dados pertinentes. 

--------------------------------------------------------------------------------------//