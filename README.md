 Descrição do Projeto
Este projeto implementa um pipeline completo de ETL (Extract, Transform, Load) na AWS, utilizando serviços gerenciados para processamento e análise de dados. A arquitetura foi desenvolvida com foco em escalabilidade, automação e boas práticas de engenharia de dados.
🏗️ Arquitetura
Amazon RDS → AWS Glue ETL → S3 Bucket → AWS Athena → User
                              ↓
                         Glue Crawler
Componentes:

Amazon RDS: Database relacional como fonte de dados estruturados e normalizados
AWS Glue ETL: Serviço de ETL serverless para transformação e processamento dos dados
S3 Bucket: Armazenamento de objetos para os dados processados (Data Lake)
AWS Glue Crawler: Catalogação automática dos dados no Data Catalog
AWS Athena: Query engine para análise dos dados via SQL
VPC & Public Subnet: Infraestrutura de rede isolada e segura

🚀 Tecnologias Utilizadas

AWS Services:

Amazon RDS (Relational Database Service)
AWS Glue (ETL & Data Catalog)
Amazon S3 (Simple Storage Service)
AWS Athena
Amazon VPC


Infrastructure as Code:

Terraform


Scripts:

Python
Bash

Conta AWS ativa
AWS CLI configurado
Terraform instalado (versão >= 1.0)
Python 3.x
Conhecimentos básicos de SQL e AWS

⚙️ Como Usar
1. Clone o repositório
bashgit clone https://github.com/valdyferreis/Data-Engineering.git
cd Data-Engineering
2. Configure as credenciais AWS
bashaws configure
3. Execute o script de setup
bashcd scripts
chmod +x setup.sh
./setup.sh
4. Provisione a infraestrutura com Terraform
bashcd terraform
terraform init
terraform plan
terraform apply
5. Execute o job do Glue ETL
Após a infraestrutura estar provisionada, execute o job do Glue através do console AWS ou CLI.
6. Consulte os dados com Athena
Acesse o AWS Athena e execute queries SQL sobre os dados processados.
📊 Funcionalidades

✅ Extração automática de dados do RDS
✅ Transformação e limpeza de dados com Glue ETL
✅ Armazenamento otimizado em S3
✅ Catalogação automática com Glue Crawler
✅ Queries SQL interativas com Athena
✅ Infraestrutura como código (IaC) com Terraform
✅ Rede isolada com VPC

🔐 Segurança

IAM Roles e Policies com princípio do menor privilégio
VPC com subnets públicas e privadas
Criptografia de dados em repouso (S3)
Logs e monitoramento habilitados

 Melhorias Futuras

 Implementar CI/CD pipeline
 Adicionar testes automatizados
 Implementar notificações SNS
 Adicionar CloudWatch Dashboards
 Implementar particionamento de dados no S3
 Adicionar data quality checks.

 Valdemar Joao
