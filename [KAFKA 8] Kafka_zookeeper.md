**[KAFKA THEORY]**

--------------------------------------------------------------------------------------//

# ZOOKEEPER

**apache "Zookeeper" é um software para coordenação de componentes internos no contexto de aplicações distribuídas em nuvem.**

* Zookeeper atual no contexto do kafka em conjunto com a engine do mesmo, para definir, qual broker sera o lider de determinada partição.

  - **mantém uma lista de todos os brokers**.
  - **envia notificações ao kafka em casos de alterações nos componentes internos**.
     - (e.g novo topico criado, broker derrubado, broker reiniciado, deleção de topicos ...)
     
* kafka 2.x nao funciona sem o zookeeper.
* kafka 3.x pode funcionar sem o zookeeper, usando kafka raft no lugar.
* kafka 4.x nao usa zookeeper (nao lancado ainda).

* só podemos ter quantidades impares de instancias do zookeeper rodando em cada servidor de uma vez (1,3,5,7)

**nao use kafka-clients (producer e consumer) em conjunto com zookeeper, pois esta descontinuado**.

**por outro lado, kafka-brokers em produção ainda devem ser usados sob gerencia do zookeeper até que seja liberado kafka 4.x**.

========================================================================
--------------------------------------------------------------------------------------//