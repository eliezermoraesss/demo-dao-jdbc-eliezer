# Acesso a banco de dados com JDBC

## Objetivo geral:
Conhecer os principais recursos do JDBC na teoria e prática <br>
Elaborar a estrutura básica de um projeto com JDBC<br>
Implementar o padrão DAO manualmente com JDBC<br>
## Visão geral do JDBC
JDBC (Java Database Connectivity): API padrão do Java para acesso a dados<br>
Páginas oficiais:<br>
https://docs.oracle.com/javase/8/docs/technotes/guides/jdbc/<br>
https://docs.oracle.com/javase/8/docs/api/java/sql/package-summary.html<br>
Pacotes: java.sql e javax.sql (API suplementar para servidores)<br>

## Instalação das ferramentas:
Instalar o MySQL Server e o MySQL Workbench<br>


## Preparação do primeiro projeto no Eclipse

### Checklist:
1. Usando o MySQL Workbench, crie uma base de dados chamada "coursejdbc"<br>
2. Baixar o MySQL Java Connector<br>
3. Caso ainda não exista, criar uma User Library contendo o arquivo .jar do driver do MySQL<br>
4. Window -> Preferences -> Java -> Build path -> User Libraries<br>
5. Dê o nome da User Library de MySQLConnector<br>
6. Add external JARs -> (localize o arquivo jar)<br>
7. Criar um novo Java Project<br>
8. Acrescentar a User Library MySQLConnector ao projeto<br><br>
9. Na pasta raiz do projeto, criar um arquivo "db.properties" contendo os dados de conexão:<br>
user=developer<br>
password=1234567<br>
dburl=jdbc:mysql://localhost:3306/coursejdbc<br>
useSSL=false<br><br>
11. No pacote "db", criar uma exceção personalizada DbException<br>
12. No pacote "db", criar uma classe DB com métodos estáticos auxiliares<br>
Obter e fechar uma conexão com o banco<br>
