# State of Data Brasil 2025/2026 — Análise Exploratória

Projeto de portfólio com uma análise exploratória e descritiva completa da pesquisa **State of Data Brasil 2025/2026** (Data Hackers/Kaggle), cobrindo desde a ingestão e tratamento dos dados até a extração de insights sobre o perfil profissional, tecnológico e salarial de quem trabalha (ou busca trabalhar) com dados no Brasil.

O foco do projeto é demonstrar o **processo analítico de ponta a ponta** — não apenas o resultado final — seguindo a metodologia **CRISP-DM**, com atenção especial a decisões de tratamento de dados que impactam diretamente a qualidade dos insights.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Gabriel-Roledo-ds/Analise-State-of-Data-2025/blob/main/Mercado_de_dados_SoD.ipynb)

## Sobre os dados

- **Fonte:** Data Hackers / Kaggle
- **Respondentes:** 3.495
- **Colunas:** 388 (majoritariamente variáveis dummy resultantes de perguntas de múltipla escolha)

## Objetivo

Realizar uma análise exploratória e descritiva orientada a insights relevantes para profissionais de dados — com um recorte especial para quem está buscando entrar na área — cobrindo:

- Perfil demográfico e educacional
- Trajetória e senioridade
- Stack tecnológica (linguagens, bancos de dados, cloud, BI, IA generativa)
- Remuneração
- Padrões de entrada no mercado

## Metodologia — CRISP-DM

Este projeto segue a metodologia **CRISP-DM** (Cross-Industry Standard Process for Data Mining), adaptada ao contexto de uma análise exploratória e descritiva (sem etapa de modelagem preditiva).

### 1. Business Understanding (Entendimento do Negócio)

Como não há um cliente ou problema de negócio real, essa etapa foi adaptada para **definição dos objetivos da análise**:

- Entender o perfil de quem trabalha (ou busca trabalhar) com dados no Brasil
- Mapear a stack tecnológica dominante no mercado
- Identificar padrões de remuneração por senioridade e cargo
- Extrair insights relevantes para profissionais buscando entrada na área

### 2. Data Understanding (Entendimento dos Dados)

- Ingestão da base *State of Data Brasil 2025/2026*
- Inspeção estrutural: tipos de dados, volume de colunas, padrão de nulos
- Identificação e validação do *skip pattern* da pesquisa (colunas dummy de múltipla escolha com NaN estrutural, não aleatório)

### 3. Data Preparation (Preparação dos Dados)

- Tratamento diferenciado por tipo de variável (dummy binária vs. categórica de resposta única)
- Definição da base de cálculo correta para percentuais (denominador ajustado por seção respondida, não pelo total de respondentes)
- Padronização e organização das colunas por grupo temático

### 4. Modeling (Modelagem)

*Não aplicável* — este projeto tem caráter descritivo/exploratório, sem construção de modelos preditivos.

### 5. Evaluation (Avaliação)

Adaptada para **validação dos insights**:

- Checagem de consistência dos padrões encontrados (ex: repetição do teste de skip pattern em múltiplos grupos de colunas)
- Verificação se os achados respondem às perguntas definidas na etapa de Business Understanding

### 6. Deployment (Implantação)

Adaptada para **comunicação dos resultados**:

- Notebook documentado e publicado no GitHub, com raciocínio analítico explicado célula a célula
- Síntese dos principais insights em formato de apresentação para LinkedIn

## Estrutura do notebook

1. **Ingestão e primeira leitura** dos dados *(Data Understanding)*
2. **Inspeção estrutural** — dicionário de variáveis e padrão de nulos *(Data Understanding)*
3. **Tratamento e limpeza** — considerando o *skip pattern* da pesquisa *(Data Preparation)*
4. **Análise exploratória** (univariada e cruzada) *(Evaluation)*
5. **Insights e conclusões** *(Deployment)*

## Destaque metodológico

Um ponto central do tratamento de dados neste projeto: a maior parte das colunas do dataset (~80%) são variáveis binárias (0/1/NaN) originadas da decomposição de perguntas de múltipla escolha. Foi identificado e validado que o `NaN` nessas colunas representa, em sua maioria, **skip pattern** (o respondente não foi exposto à pergunta) — e não dado ausente por erro de coleta. Essa distinção é essencial para o cálculo correto de qualquer percentual ao longo da análise.

## Ferramentas

- Python (pandas)
- Google Colab

## Status

🚧 Em desenvolvimento — notebook sendo construído célula a célula, com documentação do raciocínio analítico em cada etapa.
