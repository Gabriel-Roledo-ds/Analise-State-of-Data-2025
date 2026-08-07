# State of Data Brasil 2025/2026 — Análise Exploratória

Projeto de portfólio com uma análise exploratória e descritiva completa da pesquisa **State of Data Brasil 2025/2026** (Data Hackers/Kaggle), cobrindo desde a ingestão e tratamento dos dados até a extração de insights sobre o perfil profissional, tecnológico e salarial de quem trabalha (ou busca trabalhar) com dados no Brasil.

O foco do projeto é demonstrar o **processo analítico de ponta a ponta** — não apenas o resultado final — com atenção especial a decisões de tratamento de dados que impactam diretamente a qualidade dos insights.

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

## Estrutura do notebook

1. **Ingestão e primeira leitura** dos dados
2. **Inspeção estrutural** — entendimento do dicionário de variáveis e do padrão de nulos
3. **Tratamento e limpeza** — tratamento diferenciado por tipo de variável, considerando o *skip pattern* da pesquisa
4. **Análise exploratória** (univariada e cruzada)
5. **Insights e conclusões**

## Destaque metodológico

Um ponto central do tratamento de dados neste projeto: a maior parte das colunas do dataset (~80%) são variáveis binárias (0/1/NaN) originadas da decomposição de perguntas de múltipla escolha. Foi identificado e validado que o `NaN` nessas colunas representa, em sua maioria, **skip pattern** (o respondente não foi exposto à pergunta) — e não dado ausente por erro de coleta. Essa distinção é essencial para o cálculo correto de qualquer percentual ao longo da análise.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Gabriel-Roledo-ds/Analise-State-of-Data-2025/blob/main/Mercado_de_dados_SoD.ipynb)

## Ferramentas

- Python (pandas)
- Google Colab

## Status

🚧 Em desenvolvimento — notebook sendo construído célula a célula, com documentação do raciocínio analítico em cada etapa.
