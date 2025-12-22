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
