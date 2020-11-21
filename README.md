# DP-900

Data Structured: table and spreadsheet
Semi-structured: json, xml e parquet
Unstructured: image, audio, video, pdf, word

OLTP: desempenho na transacao, escrever, atualizar e deletar registro. Reduzir redundancia de dados atraves da normalizacao dos dados.
BEGIN TRANSACTION
UPDATE ...
INSERT INTO...
DELETE ...
COMMIT TRANSACTION

![alt text](https://i0.wp.com/improveandrepeat.com/wp-content/uploads/2018/12/AdvWorksOLTPSchemaVisio.png?)

OLAP: armazenamento multidimensional com Fatos e dimensões para otimizar a leitura para geração de relatórios.
Os dados podem ter origem  On-premises, cloud, SaaS e sensores processados via batch ou streaming para serem disponibilizados em relatórios e dashboards.

![alt text](https://moidulhassan.files.wordpress.com/2014/07/adventureworksdw2008.png)

DBA: gerencia banco de dados, controla acesso, realiza backups e monitora a performance. Utiliza Azure Data Studio, SQL Server Management Studio e Azure Portal/ClI.
Data Engineer: cria pipelines e prepara os dados para a analise. Utiliza Azure Synapse Studio (DW Azure), SQL Server Management Studio e Azure Portal/CLIE
Data Analyst: cria reposts e visualização de dados, modela os dados para analise e prove insights. Utiliza Power BI.

Dados Relacionais
Em uma tabela chaves primarias e estrangeiras sao utilizadas para definir relacionamentos entre tabelas e joins são utilizados para retornar dados desses relacionamentos.
Um indice otimiza a busca de dados reduzindo a quantidade de paginação necessária para ler os dados.
Uma view é uma forma de nomear uma Query facilitando a escrita de querys

DML: SELECT, INSERT, UPDATE, DELETE
DDL: CREATE, DROP, ALTER
DCL: GRANT, REVOKE, DENY

Azure Data Services
SQL Server on Azure Virtual Machines (IaaS) tem acesso completo ao OS (maior custo, esforço e controle), permite aproveitar licenças. Em relacao ao on-permise possui backup automaticos da VM (não do banco), escalonamento vertical rapido e recuperação de disastres.
Azure SQL Managed Instance (PaaS) acesso somente a Instância SQL Server
Azure SQL Database (PaaS) recurso de banco na nuvem (menor custo, esforço e controle). Serveless compute (recurso é cobrado somente quando é utilizado) e alta disponibilidade. Permite outros bancos além de SQL Server como PostgreSQL, MySQL e MariaDB

Dados Nao-relacionais
Schema nao é tabular e os dados são semi-struturados, o documento define sua propia estrutura e nome dos campos
Utilizado em IOT, streaming e aplicações de baixa latência.

Storage Account: blob, arquivos(container e fileshare) e azure table
Azure table storage usa key, value
Azure blob storage: append (ideal para log), page (HDs virutais) e block (binary objects)
CosmosDB : apis mongodb, cassandra, API SQL, azure table para consulta de dados não estruturado


NOSQL: chave-valor, grafos, baseado em documentos e column family databases. No Azure é o CosmosDB.

Dados desestruturados
Busca extrair dados da origem para serem caracterizados.Frequetemente utilizados com Machine learning e servicos cognitivos.

O Data processing normalmente é realizado por functions, databricks e cognitives no azure
ELT utiliza um DAtalake

Modern DW: combina batch e stream
Ingestão e Preparacao: Data Factory (automatizar movimentacao de dados) e Azure Databricks (Spark)
Model e Serve: Azure Synapse Analytics (consultas distribuidas)
Visualize: PowerBI
Store: Azure Data lake Sorage, compativel com HDFS
