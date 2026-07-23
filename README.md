# 🚀 Implementando Primeira Stack com AWS CloudFormation

**Bootcamp:** GFT - Fundamentos de Cloud com AWS  
**Plataforma:** [Digital Innovation One (DIO)](https://www.dio.me/)  
**Autor:** Evelyn Oliveira Bonatto  
**Status:** 🛠️ Concluído

---

## 📌 Descrição do Projeto

Este repositório contém o projeto prático do bootcamp da DIO, focado em **Infrastructure as Code (IaC)** com o **AWS CloudFormation**. O objetivo foi criar e implantar pilhas de recursos na AWS - incluindo instâncias EC2, buckets S3, regras de firewall (Security Groups) e roles de IAM, além de validar a arquitetura com testes práticos diretamente no console da AWS.

---

## 🎯 Stack Principal: EC2 + S3

Através do template principal (`template.yaml`), foram provisionados de forma automatizada e declarativa:

- **Amazon EC2**: Uma instância `t2.micro` (Amazon Linux 2023) parametrizada e elegível para o nível gratuito (Free Tier).
- **Amazon S3**: Um bucket de armazenamento privado configurado com bloqueio de acesso público (`PublicAccessBlockConfiguration`), aplicando boas práticas de segurança.

---

## 🛠️ O que foi criado em cada Stack de Teste

Além da stack principal, foram executados 4 cenários de laboratório para testar a criação e interação de diferentes serviços na AWS:

- **`Lab-EC2`**:
  - **Objetivo**: Teste básico de computação.
  - **Recursos Criados**: Provisionamento isolado de uma instância **Amazon EC2** (`t2.micro`).

- **`Lab-Apache`**:
  - **Objetivo**: Subida e configuração de um servidor web.
  - **Recursos Criados**: Instância **Amazon EC2** configurada com script de inicialização (_UserData_) para instalação e execução automática do servidor **Apache (HTTPD)**.

- **`Lab-Firewall`**:
  - **Objetivo**: Controle de tráfego e regras de rede.
  - **Recursos Criados**: Definição de um **Security Group (Grupo de Segurança)** com regras de entrada (_Inbound Rules_) para liberação de portas de acesso (ex: HTTP e SSH).

- **`Lab-EC2-IAM-S3`**:
  - **Objetivo**: Arquitetura integrada combinando computação, segurança, identidade e armazenamento.
  - **Recursos Criados**:
    - Instância **Amazon EC2**;
    - **Security Group** exclusivo para a instância;
    - **Bucket S3** para armazenamento de arquivos;
    - **Usuário e Grupo no IAM** (`IAMUser` e `IAMGroup`) para gestão refinada de permissões.

---

## 📸 Evidências de Execução

Clique nos links abaixo para conferir as capturas de tela das etapas e testes realizados no console da AWS:

- 🔗 [Visão Geral das Stacks de Teste](./images/stacks-teste.png)
- 🔗 [Recursos Mapeados na Stack Completa](./images/stack-complexo.png)
- 🔗 [Criação Concluída da Stack Principal](./images/01-stack-complete.png)
- 🔗 [Eventos de Criação do CloudFormation](./images/02-stack-events.png)
- 🔗 [Recursos Provisionados](./images/03-stack-resources.png)
- 🔗 [Saídas e Parâmetros (Outputs)](./images/04-stack-outputs.png)
- 🔗 [Instância EC2 em Execução](./images/05-ec2-running.png)

---

## 💡 Aprendizados e Insights

- **Infraestrutura em Código:** Aprendi a usar arquivos YAML no CloudFormation para criar recursos na AWS de forma automática e organizada.
- **Outputs e Versionamento:** Entendi como usar a seção de *Outputs* para reutilizar dados da stack e como organizar o Git para manter os arquivos fáceis de ler.

---

## 🧹 Limpeza de Recursos (Clean-up)

Para evitar custos indesejados na conta AWS, a remoção das stacks de teste deve ser feita no console do CloudFormation na seguinte ordem:

1. `Lab-EC2-IAM-S3`
2. `Lab-Apache`
3. `Lab-EC2`
4. `Lab-Firewall`
5. `dio-ec2-s3-stack`

---

## 🔗 Conecte-se Comigo

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/evelyn-bonatto/)
