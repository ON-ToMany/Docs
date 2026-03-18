Seguradora especializada em E-Bikes
Projeto desenvolvido para o Desafio 01 - Projeto Integrador
📚 ESCOPO DO PROJETO

Projeto: IonGuard Seguros
Modelo: Seguradora E-Bike
👥 GRUPO 01

Integrantes

Álvaro Maximiano
Breno Nunes
José Rodrigues
Mayara Gonçalves
Maria Eduarda Gomes
Márcia Telles Fogaça
Mateus Santos Vieira
1️ Nome do Projeto

IonGuard Seguros
2️ Modelo do Projeto

Seguradora veicular especializada em E-Bikes.
3️ Descrição do Projeto

A IonGuard nasceu para proteger quem escolheu o futuro da mobilidade.
Especializada em seguros para bicicletas elétricas (E-Bikes), oferecemos cobertura completa contra:
🔐 Roubo
🚨 Furto
🔧 Reparos de chassis
🔋 Problemas em baterias
Nosso objetivo é garantir que sua bicicleta elétrica esteja sempre pronta para o próximo trajeto.
🛠 4 Tecnologias Utilizadas

ItemTecnologia🖥 ServidorNode.js💻 LinguagemTypescript⚙ FrameworkNestJS🗄 ORMTypeORM🗃 Banco de DadosMySQL
📊 5 Diagrama Entidade-Relacionamento


🗄 6 Descrição das Tabelas e seus Atributos

Banco de Dados:
db_seguradora_ion_guard
SGBD: MySQL
📋 Tabela: tb_apolice

AtributoTipoDescriçãoChaveidBIGINTSuporta grande quantidade de cadastros de apólicesPKtipo_seguroVARCHAR(255)Categoria do seguro contratadoNNvalor_planoDECIMAL(5,2)Valor do plano escolhido pelo clienteNNdata_inicioDATEData de início da vigência do planoNNdata_fimDATEData final da vigência do planoNNstatus_planoVARCHAR(255)Status do plano (Adimplente, Cancelado, Inadimplente)NN
🧩 7 Descrição das Entidades e seus Atributos

Classe: apolice

AtributoTipoDescriçãoidnumberIdentificador único da apólicetipo_segurostringTipo de seguro contratadovalor_planonumberValor do planodata_iniciodateData de início da vigênciadata_fimdateData final da vigênciastatus_planostringStatus atual do plano (Ativo, Cancelado, Inadimplente)

About
Projeto Integrador 01 -Realizado durante bootcamp na Generation Brasil, para fins de aplicabilidade dos conhecimentos adquiridos.
Resources
 Readme


 Activity
 Custom properties
Stars

 0 stars
Watchers

 0 watching
Forks

 0 forks
 Audit log
Report repository
Releases
No releases published
Create a new release
Packages
No packages published
Publish your first package
Contributors3

Imayagmb

jrs-neto José Rodrigues

0NEtoMany
Footer

© 2026 GitHub, Inc.
Footer navigation
Terms
Privacy
Security
Status
Community
Doc