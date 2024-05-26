# Projeto de Deploy Contínuo no EC2 com GitHub Actions e CloudFormation
Este projeto utiliza CloudFormation para criar infraestrutura e GitHub Actions para automatizar o processo de deploy contínuo de uma aplicação Go em uma instância EC2 da AWS. O workflow realiza as seguintes etapas:

1. Faz o checkout do repositório do GitHub.
2. Configura as credenciais da AWS.
3. Implanta a infraestrutura na AWS usando o AWS CloudFormation.
4. Compila a aplicação Go.
5. Configura o agente SSH para se conectar à instância EC2.
6. Transfere o binário compilado para a instância EC2.
7. Executa o binário na instância EC2.

## Pré-requisitos
1. Uma conta AWS com permissões para criar instâncias EC2 e stacks no CloudFormation.
2. Uma chave SSH para acessar a instância EC2.
3. Armazenar as seguintes chaves no GitHub Secrets do repositório:
* AWS_ACCESS_KEY_ID
* AWS_SECRET_ACCESS_KEY
* EC2_SSH (conteúdo da chave privada)
* REMOTE_USER (usuário SSH para conectar à instância EC2)
