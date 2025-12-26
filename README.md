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

