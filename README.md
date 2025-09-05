# aws-ec2-lab
Documentação do laboratório de gerenciamento de instâncias EC2 na AWS
# Gerenciamento de Instâncias EC2 na AWS

Este repositório contém a documentação do laboratório prático para consolidar conhecimentos sobre o gerenciamento de instâncias EC2 na AWS.

## Objetivo
O objetivo deste laboratório foi aprender de forma prática a criar, configurar e gerenciar instâncias EC2, consolidando os conhecimentos adquiridos durante as aulas.


## Passo a Passo

### 1. Criação da Instância EC2
1. Faça login no console da AWS.
2. Acesse o serviço **EC2**.
3. Clique em **Launch Instance** (Iniciar Instância).
4. Configure os seguintes parâmetros:
   - Escolha uma **Imagem de Máquina Amazon (AMI)**: Utilize a Amazon Linux 2 (grátis elegível).
   - Escolha um **tipo de instância**: Selecione `t3.micro` (grátis elegível).
   - Configure o **par de chaves**:
     - Crie ou selecione um par de chaves existente.
     - Baixe o arquivo `.pem`ou `.ppk` e guarde-o em um local seguro.
   - Configure o **Security Group**:
     - Libere as portas necessárias, como:
       - Porta `22` para acesso SSH.
5. Clique em **Launch Instance** (Iniciar Instância).

### 2. Conexão à Instância via SSH
1. No terminal, navegue até o diretório onde está localizado o arquivo `.pem` do par de chaves.
2. Use o comando abaixo para se conectar à instância (substitua `<ip-da-instancia>` pelo IP público da instância):
   ```bash
   ssh -i "chave.pem" ec2-user@<ip-da-instancia>
