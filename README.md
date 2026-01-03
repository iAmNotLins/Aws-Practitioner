# Aws-Practitioner
Created for notes about Aws Practitioner lessons


# AWS PRACTITIONER — Introduction to the Cloud

## Anotações

### Definir computação em nuvem
- A entrega sob demanda de recursos de TI pela internet, com preços pré-pagos.

---

### Tipos de implantação na nuvem

- **Implantação baseada na nuvem**
  - Flexibilidade para migrar recursos existentes.
  - Possibilidade de projetar e criar novas aplicações na nuvem.
  - Uso combinado de ambientes.

- **On-premises**
  - Utiliza ferramentas de virtualização.
  - Oferece baixa latência.
  - Recursos dedicados.

- **Híbrida**
  - Integra nuvem e on-premises.
  - Ideal para aplicações legadas.
  - Atende requisitos de manutenção ou regulamentação.

---

### Seis principais benefícios da computação em nuvem

- Troca de despesas fixas por despesas variáveis.
- Economia de escala da AWS, reduzindo custos.
- Provisionamento apenas dos recursos necessários.
- Maior agilidade e rapidez.
- Redução de custos com manutenção de data centers.
- Escalabilidade global em minutos.

---

### Regiões e Zonas de Disponibilidade da AWS

- **Regiões**
  - Locais geográficos onde a AWS possui data centers.

- **Zonas de Disponibilidade**
  - Conjunto de data centers dentro de uma região.
  - Garantem redundância e alta disponibilidade.

---

### Alta disponibilidade e tolerância a falhas

- Evitam indisponibilidade do sistema.
- Garantem continuidade das operações.
- Reduzem impacto financeiro para a empresa.

---

### Modelo de responsabilidade compartilhada da AWS

- **Responsabilidade do cliente**
  - Segurança na nuvem.

- **Responsabilidade da AWS**
  - Segurança da nuvem.

- **Responsabilidade compartilhada**
  - Varia conforme o serviço.
  - Criptografia no servidor.
  - Proteção do tráfego de rede.

---

### Componentes do modelo de responsabilidade compartilhada

- Criptografia no lado do servidor.
- Proteção do tráfego de rede.
- Gerenciamento de plataforma e aplicações.
- Configuração do sistema operacional, rede e firewall.

---

## Amazon EC2

### Provisionamento e gerenciamento de computação na nuvem

- Sistemas operacionais:
  - Windows
  - Linux
- Casos de uso:
  - Aplicações internas de negócios
  - Aplicações web
  - Bancos de dados
  - Softwares de terceiros

---

### Comparação: EC2 vs servidores on-premises

- Altamente flexível.
- Econômico.
- Rápido para iniciar.

---

### Multilocação no Amazon EC2

- Instâncias EC2 são máquinas virtuais (VMs).
- Várias VMs compartilham um host físico.
- Cada VM opera de forma isolada.

---

## Perguntas — Amazon EC2

### 1. Comparação EC2 vs on-premises
- O EC2 é mais flexível, econômico e rápido de iniciar.

---

### 2. Conceito de multilocação
- Cada máquina virtual é isolada.
- Todas compartilham os recursos de um único host físico.

---

### 3. Cobrança ao interromper ou encerrar instâncias
- Apenas instâncias em execução são cobradas.
- Instâncias interrompidas ou encerradas não geram custo.

---

### 4. Informações essenciais para lançar uma instância EC2
- Tipo de instância.
- Sistema operacional.

---

## Tipos de instância do Amazon EC2

### Categorias e casos de uso

1. **Uso geral**
   - Equilíbrio entre CPU, memória e rede.
   - Ideal para aplicações comuns.
   - Bom ponto de partida.

2. **Otimizadas para computação**
   - Processamento intensivo.
   - Jogos, HPC e machine learning.

3. **Otimizadas para memória**
   - Workloads que manipulam grandes volumes de dados em memória.

4. **Computação acelerada**
   - Hardware especializado.
   - Processamento gráfico, ponto flutuante e análise de padrões.

5. **Otimizadas para armazenamento**
   - Alto desempenho de leitura e gravação local.
   - Ideal para workloads com alto throughput.

---

## Perguntas — Tipos de instância EC2

### Análise de dados em tempo real (instituição financeira)
- **Resposta:** Instância otimizada para memória.

---

### Análise de histórico de vendas (varejo)
- **Resposta:** Instância otimizada para armazenamento.
- Motivo:
  - Alta taxa de throughput.
  - Baixa latência no acesso a grandes volumes de dados.
 
    ```markdown
# COMO PROVISIONAR RECURSOS AWS

---

## Operação de Serviços na AWS

### Objetivo

Detalhar como utilizar o **Console de Gerenciamento da AWS**, a **AWS Command Line Interface (AWS CLI)** e os **SDKs da AWS** para operar os serviços da AWS.

---

## 1. Console de Gerenciamento da AWS

Interface gráfica (web) da AWS.

### Indicado para

- Iniciantes  
- Configurações pontuais  
- Visualização de recursos  

### Como usar

- Acessar via navegador  
- Criar, configurar e monitorar serviços manualmente  
- Ideal para testes, aprendizado e ajustes rápidos  

### Pontos positivos e limitações

- **Vantagem:** fácil de usar  
- **Limitação:** pouco eficiente para automação e tarefas repetitivas  

---

## 2. AWS Command Line Interface (AWS CLI)

Interface de linha de comando da AWS.

### Indicada para

- Automação  
- Scripts  
- Administração técnica  

### Como usar

- Instalar a AWS CLI no sistema  
- Configurar credenciais (Access Key e Secret Key)  
- Executar comandos para criar, listar, alterar ou excluir recursos  

### Pontos positivos e limitações

- **Vantagem:** rápida, automatizável e padronizada  
- **Limitação:** exige conhecimento técnico e comandos corretos  

---

## 3. SDKs da AWS

Bibliotecas que permitem integração da AWS em aplicações.

### Indicados para

- Desenvolvimento de software  
- Integração direta com sistemas e APIs  
- Automação avançada via código  

### Como usar

- Escolher o SDK da linguagem (Python, JavaScript, Java, etc.)  
- Autenticar com credenciais  
- Controlar serviços AWS diretamente pelo código da aplicação  

### Pontos positivos e limitações

- **Vantagem:** máximo controle e integração  
- **Limitação:** exige conhecimento de programação  

---

## Resumo rápido

- **Console** → uso manual e visual  
- **CLI** → automação via comandos  
- **SDKs** → integração direta em aplicações  

---

## Modelo de Responsabilidade Compartilhada da AWS

Na AWS, a segurança segue o modelo de **responsabilidade compartilhada**:

- **AWS** é responsável pela segurança da infraestrutura da nuvem  
- **Cliente** é responsável pela segurança dos sistemas, aplicações, dados e controles de acesso dentro da nuvem  

### Máquinas virtuais (Amazon EC2)

Em serviços não gerenciados, como o Amazon EC2, o cliente é responsável por:

- Sistema operacional  
- Atualizações e patches  
- Firewalls (Security Groups)  
- Configurações de segurança da instância  

---

## Serviços Gerenciados vs Não Gerenciados

### Serviço não gerenciado

Você controla quase tudo.

**Exemplo:** Amazon EC2

Você é responsável por:

- Sistema operacional  
- Atualizações e patches  
- Firewall (Security Groups)  
- Hardening e segurança  
- Instalação e manutenção de aplicações  

**Regra prática:**  
👉 Se você gerencia o sistema operacional, o serviço não é gerenciado.

---

### Serviço gerenciado

A AWS cuida da infraestrutura e do sistema base.

**Exemplos:**

- Amazon RDS  
- AWS Lambda  
- Amazon S3  

Você é responsável apenas por:

- Dados  
- Configuração de acesso  
- Regras de segurança  
- Lógica da aplicação  

A AWS é responsável por:

- Sistema operacional  
- Atualizações  
- Escalabilidade  
- Alta disponibilidade  

**Regra prática:**  
👉 Se você não vê o servidor nem o sistema operacional, o serviço é gerenciado.

---

## Comparação rápida

| Critério          | Não gerenciado | Gerenciado |
|------------------|---------------|------------|
| Acesso ao SO     | Sim           | Não        |
| Atualizações     | Você          | AWS        |
| Escalabilidade   | Manual        | Automática |
| Manutenção       | Alta          | Baixa      |
```
```
# Demonstração: Lançamento de uma Instância do Amazon EC2

## Objetivos

- Identificar as principais configurações necessárias ao criar uma instância EC2  
- Explicar como a AMI garante consistência e eficiência na escalabilidade de aplicações  

---

## AMI (Amazon Machine Image)

### Componentes de uma AMI

Uma AMI contém:

- Sistema operacional  
- Estrutura de armazenamento  
- Arquitetura da instância  
- Permissões de lançamento  
- Softwares e aplicações pré-instaladas  

A partir de uma única AMI, é possível criar múltiplas instâncias EC2 com configuração idêntica, garantindo padronização.

---

### Formas de Utilizar AMIs

- **AMI própria**
  - Criada sob medida
  - Configurações e softwares personalizados  

- **AMIs da AWS**
  - Imagens oficiais
  - Sistemas operacionais e softwares comuns  

- **AWS Marketplace**
  - AMIs de parceiros
  - Soluções especializadas prontas para uso  

---

### Repetibilidade e Escalabilidade

- Ambientes padronizados e reproduzíveis  
- Consistência entre desenvolvimento, testes e produção  
- Redução de erros  
- Facilidade de gerenciamento em larga escala  

---

# Modelos de Precificação do Amazon EC2

## Objetivos

- Explicar as opções de preços do EC2  
- Indicar quando usar cada modelo  
- Descrever reservas de capacidade e flexibilidade das Instâncias Reservadas  

---

## Opções de Preço

### Sob Demanda

- Paga apenas pelo uso  
- Ideal para:
  - Testes
  - Picos de acesso
  - Cargas imprevisíveis  

---

### Savings Plans

- Compromisso de 1 a 3 anos  
- Economia de até 72%  
- Indicado para workloads com uso previsível  

---

### Instâncias Reservadas (RI)

- Compromisso de 1 a 3 anos  
- Economia de até 75%  
- Formas de pagamento:
  - Total antecipado
  - Parcial
  - No final  
- Descontos aplicados de forma flexível entre tamanhos e zonas da mesma região  

---

### Instâncias Spot

- Até 90% de desconto  
- Podem ser interrompidas pela AWS a qualquer momento  
- Ideais para workloads:
  - Tolerantes a falhas
  - Tolerantes a interrupções  

---

### Hosts Dedicados

- Servidor físico exclusivo  
- Maior controle, segurança e compliance  

---

## Quando Usar Cada Modelo

- **Instâncias Sob Demanda**
  - Consumo variável ou imprevisível  

- **Savings Plans**
  - Uso previsível e contínuo  

- **Instâncias Reservadas (RI)**
  - Demanda estável por 1 a 3 anos  

- **Instâncias Spot**
  - Processamentos temporários
  - Workloads tolerantes a interrupções  

- **Reservas de Capacidade**
  - Workloads críticos
  - Necessidade de capacidade garantida  

- **Instâncias Dedicadas**
  - Uso exclusivo de parte do servidor  

- **Hosts Dedicados**
  - Controle total sobre o servidor físico  


# Scaling do Amazon EC2

## Conceitos de Escalabilidade e Elasticidade na AWS

Escalabilidade é a capacidade de um sistema crescer para atender mais demanda. Na AWS, ela ocorre de duas formas:

### Escalabilidade vertical (Scale Up)
- Aumenta os recursos da instância existente (CPU, memória, etc.).

### Escalabilidade horizontal (Scale Out)
- Aumenta a quantidade de instâncias para distribuir a carga de processamento.

Elasticidade é a capacidade de aumentar ou reduzir recursos automaticamente, de acordo com a demanda, evitando desperdício e garantindo desempenho.

---

## Ajuste de Capacidade Computacional na AWS

A AWS permite que empresas ajustem recursos de forma dinâmica, pagando apenas pelo que utilizam. Isso garante:

- Alta disponibilidade  
- Melhor desempenho sob picos de acesso  
- Otimização de custos em períodos de baixa demanda  

---

## Amazon EC2 Auto Scaling

O Amazon EC2 Auto Scaling ajusta automaticamente o número de instâncias do EC2 conforme a demanda da aplicação.

Ele funciona de duas maneiras:

### Escalonamento dinâmico
- Ajusta as instâncias em tempo real com base em métricas (CPU, requisições, etc.).

### Escalonamento preditivo
- Analisa padrões históricos e provisiona instâncias antecipadamente.

### Benefícios principais
- Alta disponibilidade  
- Resiliência  
- Escalabilidade automática  

---

## Direcionamento de Tráfego com Elastic Load Balancing

### Desafios sem balanceamento de carga
- Sobrecarga de uma única instância  
- Lentidão nas respostas  
- Falhas em picos de acesso  

### Vantagens do Elastic Load Balancing

O Elastic Load Balancing distribui o tráfego automaticamente entre várias instâncias EC2.

Principais benefícios:

- Distribuição eficiente de tráfego  
- Alta disponibilidade  
- Escalabilidade automática  
- Gerenciamento simplificado, com failover e manutenção gerenciada pela AWS  

---

## Integração entre Auto Scaling e ELB

### Baixa demanda
- Poucas instâncias são suficientes para atender as requisições.

### Alta demanda
- O ELB recebe o tráfego e o Auto Scaling adiciona novas instâncias EC2 automaticamente.

### Balanceamento contínuo
- O ELB distribui as requisições igualmente, evitando sobrecarga em uma única instância.

Essa integração garante desempenho, resiliência e uso eficiente de recursos.

---

## Sistema de Mensagens e Enfileiramento

### Amazon Simple Queue Service (SQS)

O Amazon Simple Queue Service permite envio, armazenamento e processamento assíncrono de mensagens.

Benefícios:

- Processamento desacoplado  
- Alta escalabilidade  
- Garantia de entrega das mensagens  
- Componentes não precisam estar ativos ao mesmo tempo  

---

### Amazon Simple Notification Service (SNS)

O Amazon Simple Notification Service utiliza o modelo publicação/assinatura (pub/sub).

- Publicadores enviam mensagens para tópicos SNS  
- Assinantes podem ser:
  - E-mail  
  - Funções Lambda  
  - Servidores  
  - Filas SQS  
  - Outros endpoints  

Ideal para notificações em tempo real e fan-out de mensagens.

---

## Arquiteturas Fortemente vs Fracamente Acopladas

### Fortemente acoplada
- Componentes dependem diretamente uns dos outros.

### Fracamente acoplada
- Componentes operam de forma independente, com comunicação assíncrona.

Arquiteturas fracamente acopladas são mais escaláveis, resilientes e flexíveis.

---

## Benefícios do Uso de Filas de Mensagens

O uso de filas (como o SQS):

- Desacopla sistemas  
- Permite processamento assíncrono  
- Evita falhas em cascata  
- Garante que mensagens sejam processadas quando o consumidor estiver disponível

# Computação sem Servidor — Resumo

## Tipos de Serviços Computacionais na AWS

### Não gerenciados
- Exemplo: Amazon EC2  
- A AWS gerencia apenas a infraestrutura física  
- O cliente é responsável por:
  - Sistema operacional
  - Segurança
  - Rede
  - Aplicações

### Gerenciados
- A AWS reduz a sobrecarga operacional
- Gerencia parte da infraestrutura
- O cliente ainda realiza algumas configurações e provisionamentos

<img width="685" height="434" alt="image" src="https://github.com/user-attachments/assets/f85af94c-1866-4020-8348-2e16240e8463" />

### Sem servidor (Serverless)
- Totalmente gerenciados pela AWS
- Não há necessidade de provisionar ou manter servidores
- O foco do cliente é apenas no código e na lógica da aplicação
- Exemplo: AWS Lambda

<img width="757" height="422" alt="image" src="https://github.com/user-attachments/assets/3f26ecb8-45b4-4d3b-b273-26e86aa11fb7" />

<img width="691" height="482" alt="image" src="https://github.com/user-attachments/assets/d93bb9cd-bc0e-45a7-87ed-4d3bb920af1e" />



---

## Responsabilidades na Computação sem Servidor

### Responsabilidades da AWS
- Infraestrutura
- Escalabilidade
- Disponibilidade
- Manutenção dos servidores

### Responsabilidades do Cliente
- Código da aplicação
- Lógica de negócio
- Configuração de permissões e segurança do código

A computação sem servidor permite maior agilidade, menos complexidade operacional e foco total no desenvolvimento da aplicação.

# AWS Lambda

## Conceito e Funcionalidade

- A solução **AWS Lambda** é um serviço computacional **sem servidor (serverless)**.
- Executa código em resposta a eventos **sem a necessidade de provisionar ou gerenciar servidores**.
- A AWS gerencia automaticamente:
  - Infraestrutura
  - Execução
  - Scaling
  - Alocação de recursos
- A cobrança é feita **por tempo computacional utilizado**, medido até o milissegundo.
- O desempenho pode ser otimizado ajustando o **tamanho de memória** da função.

---

## Principais Componentes do AWS Lambda

- **Funções**
  - Código que será executado
- **Gatilhos (Triggers)**
  - Eventos que acionam a função (ex: S3, API Gateway, eventos de serviços AWS)
- **Scaling**
  - Escala automática conforme o volume de solicitações

---

## Como a Solução Lambda Funciona

### 1. Upload do Código

- O código é enviado para o Lambda
- Ele é carregado como uma **função Lambda**

### 2. Definição da Origem de Evento

- A função é configurada para ser acionada por eventos como:
  - Serviços da AWS
  - Aplicações móveis
  - Requisições HTTP

### 3. Execução do Código

- O código executa **somente quando ocorre um evento**
- O runtime do Lambda:
  - Recebe os dados do evento
  - Executa a função
  - Gerencia automaticamente infraestrutura e scaling
- Não há necessidade de gerenciar servidores ou ambiente de execução

### 4. Modelo de Cobrança

- Pagamento baseado em:
  - Tempo de execução
  - Quantidade de memória alocada
- Cobrança feita até o **milissegundo**

---

# Contêineres e Orquestração na AWS

## Contêineres e Ambiente de Runtime

- Contêineres empacotam:
  - Aplicação
  - Bibliotecas
  - Runtime
  - Configurações
- Garantem que a aplicação rode da mesma forma em qualquer ambiente
- Características principais:
  - Não dependem do sistema operacional do host
  - Evitam o problema do “funciona na minha máquina”
  - São leves (compartilham o kernel do SO)
  - Podem ser executados em qualquer lugar que suporte contêineres

---

## Amazon Elastic Container Registry (Amazon ECR)

- Serviço da AWS para **armazenar e gerenciar imagens de contêiner**
- Principais funcionalidades:
  - Armazenamento seguro de imagens Docker
  - Versionamento de imagens por meio de tags
  - Controle de acesso via IAM
  - Integração direta com:
    - ECS
    - EKS
    - Fargate

---

## Orquestração com Amazon ECS e Amazon EKS

- Orquestração envolve:
  - Implantar
  - Escalar
  - Atualizar
  - Monitorar contêineres automaticamente

### Amazon Elastic Container Service (ECS)

- Orquestrador nativo da AWS
- Mais simples de configurar
- Ideal para quem busca menor complexidade operacional

### Amazon Elastic Kubernetes Service (EKS)

- Kubernetes gerenciado pela AWS
- Oferece:
  - Maior flexibilidade
  - Portabilidade entre ambientes
- Padrão amplamente utilizado no mercado

---

## AWS Fargate

- Permite executar contêineres **sem provisionar ou gerenciar servidores**
- Características principais:
  - Não há instâncias EC2, clusters ou SO para administrar
  - Pagamento apenas por CPU e memória utilizadas
  - Integração com ECS e EKS
  - Scaling automático


# Outros Serviços Computacionais

---

## AWS Elastic Beanstalk

**Objetivo:**  
Simplificar o provisionamento e o gerenciamento de ambientes de aplicação.

**Cria automaticamente:**
- Infraestrutura
- Redes
- Instâncias EC2
- Escalabilidade automática
- Balanceadores de carga

O usuário apenas envia o código da aplicação e define configurações básicas.

Permite salvar configurações de ambientes para reaproveitar implantações.

👉 Ideal para quem quer focar na aplicação e não na infraestrutura.

---

## AWS Batch

**Objetivo:**  
Executar tarefas computacionais em grande escala.

**Gerencia automaticamente:**
- Provisionamento de servidores
- Escalabilidade de recursos
- Distribuição de tarefas

Ajusta os recursos conforme a demanda.

Utiliza instâncias EC2 de forma otimizada.

👉 Ideal para processamento em lote, jobs pesados e workloads event-driven.

---

## Amazon Lightsail

**Objetivo:**  
Simplificar a hospedagem de aplicações web.

- Elimina grande parte da complexidade da infraestrutura tradicional
- Interface simples e preços previsíveis

Ideal para projetos pequenos, sites e aplicações simples.

👉 Ótima opção para quem quer algo rápido e fácil de gerenciar.

---

## AWS Outposts

**Objetivo:**  
Estender os serviços da AWS para ambientes locais.

- Leva a infraestrutura e os serviços da AWS para o datacenter local
- Oferece experiência unificada entre on-premises e AWS

Atende necessidades como:
- Baixa latência
- Residência de dados
- Arquiteturas híbridas

👉 Ideal para cenários de nuvem híbrida.

---

# Escolha de Regiões AWS

## Fatores para escolha de uma Região

### 1️⃣ Conformidade
Exigências legais e regulatórias (LGPD, GDPR, dados financeiros).  
➡️ Se houver obrigação legal, a região é obrigatória.

### 2️⃣ Proximidade (latência)
Quanto mais próxima dos usuários, menor o tempo de resposta.

### 3️⃣ Disponibilidade de serviços
Nem todos os serviços estão disponíveis em todas as regiões.

### 4️⃣ Custo
Os preços variam conforme impostos e custos operacionais locais.

---

# Infraestrutura Global da AWS

## Benefícios do uso de várias Regiões e Zonas de Disponibilidade

### Multi-AZ
- Uso de múltiplas AZs dentro da mesma região
- Protege contra falha de um data center
- Baixa latência entre AZs
- Gerenciado por serviços como RDS, ELB e ECS

**Quando usar:**  
Alta disponibilidade e failover automático.

---

### Multi-Região
- Uso de múltiplas regiões geográficas
- Isolamento total entre regiões
- Protege contra falha de uma região inteira
- Maior complexidade e latência

**Quando usar:**  
Disaster Recovery, aplicações globais e alta resiliência.

---

## Locais da borda (Edge Locations)

- Pontos distribuídos globalmente (ex.: Atlanta, Xangai)
- Fornecem baixa latência para entrega de conteúdo e acesso a serviços
- Aproximam os dados do usuário final

---

## Diferença entre os conceitos

- **Região:** área geográfica isolada
- **Zona de Disponibilidade (AZ):** data center redundante dentro da região
- **Local da borda:** entrega rápida de conteúdo perto do usuário

---

# Infraestrutura e Automação

## AWS CloudFormation

**Objetivo:**  
Infraestrutura como Código (IaC).

**Principais recursos e benefícios:**
- Templates em YAML ou JSON
- Provisionamento automatizado
- Controle de versão
- Atualizações consistentes
- Rollback automático
- Redução de erros manuais
- Repetibilidade entre ambientes (dev, teste, prod)

👉 Infraestrutura previsível, auditável e escalável.

---

## Formas de acesso à AWS

### Acesso programático
- AWS CLI
- AWS SDKs

**Casos de uso:**
- Automação DevOps
- Pipelines CI/CD
- Scripts e integrações
- Infraestrutura como código

---

### Console de Gerenciamento da AWS
- Interface gráfica (web)

**Casos de uso:**
- Aprendizado
- Testes
- Configurações pontuais
- Monitoramento visual

---

## Infraestrutura como Código (IaC)

**Modelo declarativo**

- CloudFormation (nativo)

**Casos de uso:**
- Ambientes padronizados
- Deploys repetíveis
- Escala profissional
- Governança e auditoria

---

# VPC e Sub-redes

## O que é uma VPC

A Amazon Virtual Private Cloud (VPC) é uma rede virtual isolada dentro da AWS.

**Controle total de:**
- Endereços IP
- Sub-redes
- Tabelas de rota
- Regras de segurança

Funciona como um data center virtual.

Permite separar ambientes (prod, dev, teste).

---

## O que é uma sub-rede

- Um “pedaço” da VPC para organizar recursos
- Agrupa recursos com funções ou níveis de acesso semelhantes
- Facilita controle de tráfego e segurança

---

## Sub-rede pública vs privada

### Sub-rede pública
- Possui rota para a internet
- Usada por sites e APIs

### Sub-rede privada
- Sem acesso direto à internet
- Usada por bancos de dados e sistemas internos

👉 Distribuídas entre AZs para segurança, organização e alta disponibilidade.

# Amazon VPC, Gateways e Conectividade

---

Uma **VPC** é o “escudo” em volta dos seus recursos na AWS.  
Dentro dela, você organiza tudo em **sub-redes** e controla o acesso usando **gateway da internet** e **gateway privado virtual (VPN)**.

---

## Objetivos da Lição

- Definir o que é um gateway privado virtual e o que ele faz  
- Identificar os principais componentes de uma VPC  
- Definir o que é um gateway da internet e o que ele faz  

---

## Amazon VPC e Sub-redes

### VPC (Virtual Private Cloud)

- Seção isolada da nuvem AWS onde você cria sua própria rede virtual
- Permite configurar:
  - Endereços IP
  - Sub-redes
  - Tabelas de rotas
  - Regras de segurança

**Benefícios principais:**
- Mais segurança (proteger, monitorar e restringir conexões)
- Mais controle sobre posicionamento e conectividade
- Menor tempo de configuração em comparação ao on-premises

---

### Sub-rede

- Subseção da VPC onde ficam recursos como instâncias EC2
- Usada para organizar e separar:
  - Recursos públicos
  - Recursos privados

---

## Gateway da Internet

- Para permitir acesso da internet pública à VPC, é obrigatório anexar um gateway da internet à VPC
- Funciona como a “porta da cafeteria”:
  - Sem ele, ninguém da internet consegue acessar recursos na VPC
  - Mesmo que os recursos existam e tenham IP público

---

## Gateway Privado Virtual e VPN

- A internet é como uma rua pública aberta a todos
- Isso não é aceitável para tráfego sensível entre a empresa e a AWS

### VPN (Virtual Private Network)

- Túnel seguro e criptografado pela internet
- Esconde o tráfego de outros usuários e provedores

### Gateway Privado Virtual

- Componente na AWS que recebe o tráfego criptografado da VPN
- Conecta esse tráfego à VPC
- Aceita apenas tráfego vindo de redes aprovadas:
  - Data center on-premises
  - Rede corporativa

---

## Diferenças de Siglas (Fichas de Conceito)

- **VPC (Virtual Private Cloud)**  
  Nuvem privada virtual, o “escudo” que isola seus recursos

- **Gateway privado virtual**  
  Ponto seguro dentro da AWS onde a VPN termina

- **Conexão VPN**  
  Túnel criptografado entre sua rede e a VPC

---

## Dica de Prova

Se a empresa quer conectar o data center corporativo à AWS pela internet, de forma segura e mantendo os recursos isolados do público, a melhor solução é:

- Gateway privado virtual  
- Conexão VPN  
- Sub-rede privada na VPC  

---

# Formas de Conexão com a AWS

Há quatro principais maneiras de se conectar à nuvem AWS nesta lição:

- AWS Client VPN
- AWS Site-to-Site VPN
- AWS PrivateLink
- AWS Direct Connect

---

## Objetivos da Lição (Conectividade)

- Descrever AWS Client VPN e quando usar  
- Descrever AWS Site-to-Site VPN e quando usar  
- Descrever AWS PrivateLink e quando usar  
- Descrever AWS Direct Connect e quando usar  

---

## AWS Client VPN

- Serviço de VPN gerenciada para conectar:
  - Profissionais remotos
  - Redes on-premises
- Totalmente gerenciado e elástico

**Benefícios:**
- Autenticação avançada
- Acesso remoto seguro
- Sem necessidade de gerenciar hardware
- Escala automaticamente conforme o número de usuários

**Caso de uso típico:**
- Acesso seguro para muitos funcionários remotos aos recursos na AWS

---

## AWS Site-to-Site VPN

- Conexão segura e criptografada entre:
  - Data centers on-premises
  - Filiais
  - Amazon VPC

**Benefícios:**
- Alta disponibilidade
- Sessões seguras e privadas
- Melhor desempenho sobre conexão criptografada

**Casos de uso:**
- Migração de aplicações
- Comunicação segura contínua entre sites e a VPC

---

## AWS PrivateLink

- Conecta sua VPC de forma privada a serviços e recursos
- Funciona como se os serviços estivessem dentro da própria VPC

**Características:**
- Não exige:
  - Gateway da internet
  - NAT
  - IP público
  - VPN
  - Direct Connect

**Benefícios:**
- Tráfego protegido
- Gerenciamento de acesso simplificado

**Caso de uso:**
- Expor serviços de forma privada para outras VPCs ou contas

---

## AWS Direct Connect

- Conexão privada dedicada entre:
  - Rede on-premises
  - AWS

**Características:**
- Não passa pela internet pública

**Benefícios:**
- Menor latência
- Conexão mais consistente
- Maior largura de banda
- Redução de custos de rede

**Casos de uso:**
- Aplicações sensíveis à latência
- Migração ou transferência de grandes volumes de dados
- Arquiteturas híbridas de longo prazo

---

## Dicas de Prova

- Migração em grande escala + alta largura de banda + conexão híbrida contínua  
  **Melhor opção:** AWS Direct Connect

- Conectar data center corporativo a sub-rede privada, aceitando apenas tráfego protegido e aprovado  
  **Melhor opção:** Gateway privado virtual + VPN Site-to-Site

---

# Tipos de Gateways na AWS

Os gateways são pontos de entrada e saída da sua rede na AWS. Cada tipo resolve um problema específico.

---

## Gateway da Internet

- Permite comunicação entre:
  - Recursos em sub-rede pública
  - Internet pública
- Sem ele, não há tráfego direto de/para a internet

---

## Gateway Privado Virtual

- Termina uma VPN Site-to-Site dentro da VPC
- Aceita apenas tráfego criptografado e de redes aprovadas
- Ideal para conectar sub-redes privadas a redes on-premises

---

## AWS Transit Gateway

- Conecta múltiplas VPCs e redes on-premises em um hub central
- Simplifica o roteamento em ambientes grandes

**Destaque:**
- Suporta peering inter-regional usando a infraestrutura global da AWS

---

## Gateway NAT

- Permite que instâncias em sub-redes privadas:
  - Acessem a internet
  - Consumam serviços externos

**Características:**
- Tráfego apenas de saída
- Nenhuma conexão pode ser iniciada da internet para as instâncias

---

## Amazon API Gateway

- Serviço gerenciado para criar, publicar e proteger APIs
- Atua como “porta de entrada” lógica das APIs

**Função:**
- Controlar como sistemas externos acessam aplicações na AWS

---

## Dica Final de Prova (Gateways)

- Conectar sub-rede privada à internet com saída apenas  
  **Gateway NAT**

- Permitir acesso direto da internet a recursos públicos  
  **Gateway da Internet**

- Conectar sub-rede privada a data center com tráfego seguro  
  **Gateway Privado Virtual**


# Sub-redes, ACLs de Rede e Grupos de Segurança na VPC

---

Sub-redes organizam recursos dentro da VPC.  
**ACLs de rede** controlam o tráfego no nível da sub-rede (**stateless**).  
**Grupos de segurança** controlam o tráfego no nível do recurso (**stateful**).

---

## Objetivos da Lição

- Descrever como o tráfego de rede funciona em uma VPC  
- Explicar como funcionam grupos de segurança (stateful)  
- Explicar como funcionam ACLs de rede (stateless)  
- Definir quem protege sub-redes usando grupos de segurança e ACLs no modelo de responsabilidade compartilhada  

---

## Sub-redes (Públicas e Privadas)

- **Sub-rede**: seção da VPC onde você agrupa recursos conforme necessidades operacionais e de segurança  
- Podem ser **públicas** ou **privadas**

**Exemplos:**
- Sub-rede pública: recursos acessíveis ao público (ex.: site da loja)
- Sub-rede privada: recursos acessíveis apenas pela rede privada (ex.: banco de dados de clientes)

Você define regras para permitir comunicação entre sub-redes, como:
- EC2 em sub-rede pública acessando banco de dados em sub-rede privada

---

## Tráfego de Rede na VPC

- Um cliente faz uma requisição
- A requisição vira um pacote
- O pacote entra na VPC pelo gateway da internet
- Antes de entrar ou sair de uma sub-rede, o pacote passa por verificações
- A **ACL de rede** associada à sub-rede decide permitir ou negar o tráfego com base em:
  - Origem
  - Tipo de comunicação

---

## ACLs de Rede (Network ACLs)

- Firewall virtual no nível da sub-rede
- Controla tráfego de **entrada** e **saída**

**Analogia:**
- Viajantes (pacotes)
- Oficial da alfândega (ACL)
- Checagem ocorre tanto na entrada quanto na saída

**Tipos:**
- ACL padrão:
  - Permite todo tráfego de entrada e saída até ser modificada
- ACL personalizada:
  - Nega todo tráfego por padrão
  - Você precisa permitir explicitamente

Todas as ACLs possuem uma **regra final de negação explícita**.

---

## ACLs de Rede — Stateless

- Filtragem **stateless**
- Não “lembram” de requisições anteriores
- Cada pacote é avaliado individualmente
- Verificação ocorre nos dois sentidos (entrada e saída)

**Consequência:**
- Para permitir tráfego de retorno, é necessário criar regras:
  - De entrada
  - De saída

---

## Grupos de Segurança

- Firewall virtual no nível do recurso (ex.: instância EC2)
- Controla tráfego de entrada e saída de recursos específicos

**Comportamento padrão:**
- Nega todo tráfego de entrada
- Permite todo tráfego de saída

**Analogia:**
- Porteiro de um prédio
- Confere a lista para entrada
- Não precisa conferir para saída

---

## Grupos de Segurança — Stateful

- Filtragem **stateful**
- Lembram decisões anteriores
- Se a entrada for permitida:
  - O tráfego de resposta é automaticamente permitido
  - Não precisa de regra adicional para retorno

**Observações:**
- Várias instâncias EC2 podem compartilhar o mesmo grupo de segurança
- Ou usar grupos diferentes, conforme o nível de controle desejado

---

## Comparação Mental: Grupos de Segurança x ACLs

- **Escopo**
  - Grupo de segurança: instância
  - ACL: sub-rede

- **Estado**
  - Grupo de segurança: stateful
  - ACL: stateless

- **Regras**
  - Grupo de segurança: apenas permitir
  - ACL: permitir e negar

- **Tráfego de retorno**
  - Grupo de segurança: permitido automaticamente
  - ACL: precisa de regras nos dois sentidos

---

## Responsabilidade na Segurança

No modelo de responsabilidade compartilhada:

- Configurar:
  - Grupos de segurança
  - ACLs de rede
- Proteger:
  - Sub-redes
  - Recursos dentro da VPC

➡️ **Responsabilidade do cliente (você)**

Esses componentes são as defesas essenciais para proteger o tráfego de rede e atender os requisitos de segurança das aplicações.

<img width="759" height="531" alt="image" src="https://github.com/user-attachments/assets/c9084f54-ff75-401e-9f70-4c8d8b81f4dd" />


# Arquiteturas Globais

---

## 1. Quando usar VPN ou Direct Connect

### VPN (Virtual Private Network)

- Conexão criptografada pela internet
- Menor custo
- Menor largura de banda
- Indicada para dados menos críticos

---

### AWS Direct Connect

- Conexão dedicada (linha física)
- Maior largura de banda
- Desempenho crítico para aplicações
- Melhor para dados sensíveis e requisitos de conformidade

---

## 2. Funcionamento em Alto Nível (VPN e Direct Connect)

### Funcionamento Conjunto

- Ambas conectam:
  - Data center corporativo → AWS
- VPN:
  - Usa a internet pública
  - Tráfego criptografado
- Direct Connect:
  - Conexão privada dedicada
  - Termina em um gateway privado virtual
- Podem ser usadas simultaneamente para:
  - Failover
  - Redundância

---

### Caso de Uso: Failover com Direct Connect

- Múltiplas conexões Direct Connect para redundância
- Agregação de largura de banda:
  - Combinar vários Direct Connects
- Essencial para:
  - Transferências pesadas de dados
  - Ambientes corporativos críticos

---

## 3. Arquitetura Multirregional com CloudFront e Route 53

### Amazon CloudFront

- Entrega conteúdo para múltiplas regiões
- Cache em edge locations
- Baixa latência
- Distribuição global de conteúdo

---

### Amazon Route 53

- Serviço DNS
- Direciona tráfego para diferentes regiões
- Roteamento inteligente de requisições
- Atua em conjunto com o CloudFront

---

### Application Load Balancer + Auto Scaling

- Balanceia carga de requisições
- Distribui tráfego entre instâncias
- Escala instâncias EC2 sob demanda

---

# Resumo de Recursos — Módulo 5: Redes

## Recursos de Infraestrutura de Rede

### 1. Amazon Virtual Private Cloud (VPC)

- Seção logicamente isolada da nuvem AWS
- Permite criar redes virtuais personalizadas
- Base de toda a arquitetura de rede na AWS

---

### 2. Sub-rede (Subnet)

- Seção de uma VPC que contém recursos
- Organiza e compartimentaliza recursos
- Pode ser:
  - Pública (com acesso à internet)
  - Privada (sem acesso direto)

---

### 3. Gateway da Internet

- Conecta a VPC à internet
- Permite tráfego público de entrada e saída
- Essencial para recursos públicos

---

### 4. Gateway Privado Virtual

- Permite tráfego protegido da internet para a VPC
- Conecta VPC a redes privadas aprovadas
- Usado em conexões VPN seguras

---

## Serviços de Conectividade

### 5. AWS Client VPN

- Conecta trabalhadores remotos à AWS
- Serviço VPN totalmente gerenciado
- Escala automaticamente conforme usuários

---

### 6. AWS Site-to-Site VPN

- Conexão segura entre:
  - Data center
  - Filiais
  - AWS
- Criptografada pela internet pública

---

### 7. AWS PrivateLink

- Conexão privada entre VPCs e serviços
- Não usa internet pública
- Faz os serviços parecerem locais à VPC

---

### 8. AWS Direct Connect

- Conexão privada dedicada
- Alta largura de banda
- Desempenho consistente
- Conexão exclusiva

---

## Recursos de Segurança

### 9. Network ACLs (ACLs de Rede)

- Controlam tráfego de entrada e saída
- Nível da sub-rede
- Filtragem stateless
- Permitem e negam tráfego explicitamente

---

### 10. Grupos de Segurança

- Controlam tráfego no nível da instância
- Filtragem stateful
- Permitem apenas regras de autorização
- Mais próximos do recurso protegido

---

## DNS e Distribuição de Conteúdo

### 11. DNS (Sistema de Nomes de Domínio)

- Traduz nomes legíveis em endereços IP
- Exemplo:
  - www.exemplo.com → 192.0.2.0

---

### 12. Amazon Route 53

- Serviço DNS escalável
- Direciona usuários para aplicações
- Suporta:
  - Registro de domínios
  - Health checks
  - Roteamento avançado

---

### 13. Amazon CloudFront

- CDN global da AWS
- Cache em edge locations
- Baixa latência
- Alta velocidade de entrega

---

## Serviços Avançados de Rede

### 14. AWS Global Accelerator

- Melhora desempenho e disponibilidade global
- Usa a rede global da AWS
- Ideal para aplicações críticas globais

---

### 15. Amazon Transit Gateway

- Hub central de conectividade
- Conecta múltiplas VPCs e redes on-premises
- Simplifica arquiteturas complexas

---

### 16. Gateway NAT

- Permite saída para a internet a partir de sub-redes privadas
- Não permite conexões iniciadas externamente
- Mantém instâncias privadas protegidas

---

### 17. Amazon API Gateway

- Criação e gerenciamento de APIs
- Altamente escalável
- Protege e monitora chamadas de API
- Gerencia todo o fluxo de requisições

---

## Tabela Comparativa Rápida

- **Security Groups**
  - Nível: Instância
  - Tipo: Stateful
  - Uso: Proteção individual de recursos

- **Network ACLs**
  - Nível: Sub-rede
  - Tipo: Stateless
  - Uso: Controle de tráfego em nível de rede

- **VPN (Client)**
  - Nível: Acesso remoto
  - Tipo: Criptografado
  - Uso: Trabalhadores remotos

- **VPN (Site-to-Site)**
  - Nível: Filial / Data center
  - Tipo: Criptografado
  - Uso: Integração on-premises

- **Direct Connect**
  - Nível: Dedicado
  - Tipo: Privado
  - Uso: Alta largura de banda e conformidade

- **CloudFront**
  - Nível: Global
  - Tipo: Cache
  - Uso: Distribuição de conteúdo

- **Route 53**
  - Nível: Global
  - Tipo: DNS
  - Uso: Roteamento de tráfego


# Introdução ao Armazenamento

Nesta lição, você aprenderá a:

---

## Conceitos de Armazenamento

### Armazenamento em Blocos

- Volume de baixa latência ligado à instância EC2
- Funciona como um “HD” ou SSD
- Ideal para:
  - Dados estruturados
  - Disco do sistema
  - Bancos de dados

### Armazenamento de Objetos

- Dados guardados como objetos em espaço de endereçamento plano
- Altíssima escalabilidade
- Metadados ricos
- Ideal para:
  - Dados não estruturados
  - Logs
  - Imagens
  - Backups

### Armazenamento de Arquivos

- Sistema de arquivos compartilhado via rede
- Permite múltiplas instâncias ou usuários acessando os mesmos arquivos simultaneamente

---

## Serviços AWS por Tipo de Armazenamento

### Blocos

- Armazenamento de instância do Amazon EC2
  - Não gerenciado
  - Temporário
  - Alto desempenho
- Amazon EBS
  - Serviço gerenciado
  - Volumes persistentes

### Objetos

- Amazon S3
  - Serviço principal de armazenamento de objetos
  - Totalmente gerenciado
  - Altamente escalável

### Arquivos

- Amazon EFS
  - NFS totalmente gerenciado
- Amazon FSx
  - Sistemas de arquivos como:
    - Windows
    - Lustre
    - NetApp ONTAP

---

## Modelo de Responsabilidade Compartilhada no Armazenamento

- Os serviços de armazenamento podem ser:
  - Totalmente gerenciados
  - Gerenciados
  - Não gerenciados
- A divisão de responsabilidades varia conforme o serviço:
  - Infraestrutura
  - Patching
  - Administração

### Responsabilidades

- Cliente:
  - Segurança dentro da nuvem
  - Configurações
  - Controle de acesso
  - Criptografia de dados
- AWS:
  - Segurança da nuvem
  - Infraestrutura física
  - Fundação dos serviços

---

# Armazenamento de Instâncias do EC2 e Amazon Elastic Block Store (Amazon EBS)

Nesta lição, você aprenderá a:

---

## Armazenamento de Instância do Amazon EC2

### Características

- Armazenamento local em blocos
- Fisicamente conectado ao host da instância EC2
- Não é um serviço separado da AWS

### Comportamento dos Dados

- Dados são temporários
- Se a instância for interrompida ou encerrada:
  - Todo o conteúdo é perdido

### Casos de Uso

- Buffers
- Caches
- Arquivos temporários
- Workloads que toleram perda de dados

### Benefícios

- Alta performance de E/S
- Custo reduzido
- Disponível automaticamente em muitos tipos de instância

---

## Amazon Elastic Block Store (Amazon EBS)

### Características

- Serviço de armazenamento em blocos persistente
- Anexado a instâncias EC2 como um disco externo

### Persistência dos Dados

- Dados permanecem mesmo se a instância for interrompida ou encerrada
- Desde que o volume não seja excluído

### Casos de Uso

- Bancos de dados
- Sistemas de arquivos
- Backups
- Ambientes de desenvolvimento clonados a partir de snapshots

### Benefícios

- Baixa latência consistente
- Redimensionamento de volumes
- Criação de snapshots
- Movimentação entre instâncias
- Suporte a:
  - Migração
  - Recuperação de desastres
  - Ajuste de performance e custos
