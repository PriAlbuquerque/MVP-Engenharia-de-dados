# MVP-Engenharia-de-dados

Este projeto foi desenvolvido como parte da Sprint: Engenharia de Dados (40530010057_20250_01).  
Foram abordadas as etapas de coleta, modelagem, carga e análise dos dados extraídos da base Scopus, visando mapear colaborações científicas, avaliar o impacto das publicações e identificar financiamentos na pesquisa.

O trabalho completo está disponível no repositório, [clique aqui para acessar o PDF completo](./Descritivo_MVP_ED_Priscila_Albuquerque.pdf).

Link para o Notebook Databricks: https://databricks-prod-cloudfront.cloud.databricks.com/public/4027ec902e239c93eaaa8714f173bcfc/4155913850843846/4135350994563997/813283758128064/latest.html


## Sumário
- [Objetivo do Projeto](#objetivo-do-projeto)
- [Coleta de Dados](#coleta-de-dados)
- [Modelagem dos Dados](#modelagem-dos-dados)
- [Catálogo de Dados](#catálogo-de-dados)
- [Carga dos Dados](#carga-dos-dados)
- [Análise dos Dados](#análise-dos-dados)
- [Autoavaliação](#autoavaliação)
- [Referências](#referências)
- [Documentação Completa](#documentação-completa)

## Objetivo do Projeto
O projeto tem como foco:
- **Quantificar** a produção científica brasileira na área de Medicina entre 2005 e 2021.
- **Mapear** parcerias de colaboração científica, nacionais e internacionais.
- **Avaliar** o impacto das publicações através de indicadores bibliométricos.
- **Investigar** o financiamento da pesquisa com base nas menções e agradecimentos nos artigos.

## Coleta de Dados
A coleta foi realizada a partir do banco de dados Scopus utilizando a API da *Pybliometrics*. Os principais passos foram:
- Seleção de publicações na área de Medicina com pelo menos um autor afiliado a uma instituição brasileira.
- Execução da coleta separadamente para cada ano do período para atender às limitações da API.
- Armazenamento dos dados brutos na camada Bronze para posterior transformação.

## Modelagem dos Dados
A modelagem dos dados seguiu uma abordagem em camadas inspirada na arquitetura Data Lakehouse:
- **Camada Bronze:** Armazenamento dos dados brutos extraídos.
- **Camada Silver:** Processos de limpeza, padronização e transformação dos dados.
- **Camada Gold:** Consolidação dos dados em um modelo dimensional (esquema estrela) para facilitar análises robustas.

## Catálogo de Dados
O **Catálogo de Dados** é um elemento fundamental deste projeto. Ele documenta de forma detalhada o modelo dimensional implementado na camada Gold, listando as tabelas, atributos (com tipos e descrições) e os relacionamentos entre elas. Essa documentação garante:
- **Clareza e Transparência:** Facilita a compreensão e o uso dos dados por toda a equipe e partes interessadas.
- **Manutenção e Evolução:** Serve como referência para atualizações e melhorias futuras, promovendo a integridade e a consistência das informações.
- **Validação:** Auxilia na verificação da qualidade dos dados, sustentando análises críticas e decisões baseadas em evidências.
Apresentado no pdf descritivo do projeto. [clique aqui para acessar o PDF completo](./Descritivo_MVP_ED_Priscila_Albuquerque.pdf).

## Carga dos Dados
Os dados foram carregados e integrados utilizando scripts em Python e PySpark, executados na plataforma Databricks. Essa etapa contemplou:
- Ingestão dos dados brutos.
- Transformação e limpeza com o uso de funções em PySpark e consultas SQL.
- Consolidação dos dados transformados na camada Gold para permitir análises rápidas e precisas.

## Análise dos Dados
A análise realizada envolveu:
- **Qualidade dos Dados:** Verificação de integridade, completude e ausência de duplicidades.
- **Impacto das Publicações:** Quantificação dos artigos, identificação das principais colaborações e mapeamento dos artigos mais citados.
- **Financiamento:** Avaliação das fontes de financiamento e das parcerias entre agências nacionais e internacionais.

## Autoavaliação
Durante o desenvolvimento do projeto, os desafios iniciais foram superados por meio do estudo contínuo e da aplicação prática dos conceitos de engenharia de dados. Essa experiência contribuiu significativamente para o aprimoramento das habilidades técnicas e analíticas.

## Referências
1. Baas, J. et al. "Scopus as a curated, high-quality bibliometric data source for academic research in quantitative science studies."  
2. Rose, M.E. e Kitchin, J. "pybliometrics: Scriptable bibliometrics using a Python interface to Scopus."  
3. Databricks Community Edition – Plataforma utilizada para processamento dos dados.

## Documentação Completa
Para detalhes adicionais sobre o desenvolvimento do projeto, consulte a documentação completa disponível em PDF:  
[Descritivo_MVP_ED_Priscila_Albuquerque.pdf](./Descritivo_MVP_ED_Priscila_Albuquerque.pdf)
