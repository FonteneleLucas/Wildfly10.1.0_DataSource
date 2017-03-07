# Wildfly10.1.0_DataSource
Como configurar DataSource Mysql no Wildfly 10. 

Fazer download do Mysql_connector usando Maven:

<dependencies>
...
  <dependency>
      <groupId>mysql</groupId>
      <artifactId>mysql-connector-java</artifactId>
      <version>6.0.4</version>
  </dependency>
</dependencies>

*Construir com dependências
É necessario copiar o Mysql-Connertor. Que foi baixado com o Maven no seguinte diretorio: 
C:\Users\seuUser\ .m2\repository\mysql\mysql-connector-java
E colar dentro da pasta  main no diretorio juntamente com o module.xml
diretorioDo(module & mysql-connector)\wildfly-10.1.0.Final\modules\system\layers\base\com\mysql\Driver\main
Após isso com o servidor desligado, vamos no direitorio: ...wildfly-10.1.0.Final\standalone\configuration
e editar o     standalone-full.xml    
Pesquisar por datasource, e acrescentar as linhas que estão especificadas no arquivo standalone-full.xml do repositorio.

