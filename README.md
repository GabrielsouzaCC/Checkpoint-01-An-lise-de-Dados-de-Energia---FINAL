#  Análise de Dados de Energia — SERS / FIAP
 
**Curso:** Ciência da Computação  
**Disciplina:** Soluções em Energias Renováveis e Sustentáveis  
**Instituição:** FIAP  
 
---
 
##  Sobre o Projeto
 
Este repositório reúne as atividades práticas de análise de dados do setor de energia elétrica desenvolvidas nas aulas 03, 04 e como desafio final da disciplina de Soluções em Energias Renováveis e Sustentáveis (SERS).
 
O objetivo geral é aplicar técnicas de preparação, manipulação e interpretação de dados reais do setor energético utilizando **Python**, **Pandas**, **Matplotlib** e **Orange Data Mining**, sem o uso de modelos de aprendizado de máquina — o foco está na análise exploratória e nos indicadores estatísticos.
 
---
 
## Estrutura do Repositório
 
```
 analise-dados-energia-sers
 ┣  desafio_final.ipynb          ← Desafio Final: API pública do ONS
 ┣  exercicios_aulas_03_04.ipynb ← Exercícios das Aulas 03 e 04
 ┗   README.md                    ← Este arquivo
```
 
---
 
##  Descrição dos Arquivos

###  `desafio_final.ipynb`
 
Notebook com a resolução completa do Desafio Final da disciplina.
 
**Situação-problema:** Uma equipe de planejamento energético precisa analisar o comportamento da carga elétrica da área de São Paulo, utilizando dados reais obtidos diretamente de uma API pública do Operador Nacional do Sistema Elétrico (ONS).
 
| Desafio | O que foi feito |
|---------|----------------|
| 1 | Criação do DataFrame a partir da resposta da API. Inspeção com `head()`, `shape`, `info()` e `describe()`. |
| 2 | Renomeação de atributos, seleção de colunas relevantes, verificação de valores ausentes e conversão de tipos. |
| 3 | Cálculo de indicadores: carga mínima, máxima, média, mediana e amplitude. |
| 4 | Identificação de períodos de alta demanda (acima de 90% do máximo). Localização do pico histórico. |
| 5 | Segundo critério de análise definido pela equipe: registros com carga acima da média. |
| 6 | Dois gráficos: série temporal da carga e histograma de distribuição. |
| 7 | Variável `resumo_resultados` com todos os indicadores calculados. |
| 8 | Relatório técnico gerado com base nos resultados produzidos pela equipe. |
 
---
 
###  `exercicios_aulas_03_04.ipynb`
 
Notebook com a resolução dos exercícios práticos das aulas 03 e 04, utilizando o **Dataset 1 — Appliances Energy Prediction (UCI)**.
 
**Situação-problema:** Uma empresa de eficiência energética analisa o comportamento de uma residência de baixo consumo. A equipe deseja identificar os períodos de consumo elevado dos eletrodomésticos e observar quais condições de temperatura e umidade estavam presentes nesses momentos.
 
**Etapa A — Orange Data Mining:**
- Carregamento do arquivo CSV no widget File
- Inspeção dos atributos no Data Table
- Seleção de colunas: `Appliances`, `lights`, temperaturas (T1, T2, T3) e umidades (RH_1, RH_2, RH_3)
- Verificação de valores ausentes
- Geração de amostra aleatória de **10%** com Data Sampler
- Exportação da amostra como `amostra.csv`
**Etapa B — Python / Pandas:**
- Carregamento da amostra e inspeção inicial
- Renomeação dos atributos para nomes mais claros
- Cálculo do maior consumo registrado
- Filtro de alta demanda: registros acima de **70% do consumo máximo**
- Cálculo de quantidade e percentual de registros filtrados
- Segundo critério: consumo elevado **e** temperatura acima da média simultaneamente
- Comparação e interpretação dos dois conjuntos
- Gráfico da distribuição do consumo
---
 
##  Fontes dos Dados
 
### Desafio Final — ONS (Operador Nacional do Sistema Elétrico)
 
| Item | Detalhe |
|------|---------|
| Portal oficial | https://dados.ons.org.br/ |
| Dataset | Carga Verificada do ONS |
| Endpoint da API | https://apicarga.ons.org.br/prd/cargaverificada |
| Área analisada | SP — São Paulo |
| Período | 01/08/2025 a 07/08/2025 |
| Formato | JSON via requisição HTTP GET |
 
O ONS é o órgão responsável pela coordenação e controle da operação das instalações de geração e transmissão de energia elétrica no Sistema Interligado Nacional (SIN). Os dados de carga verificada representam o consumo real medido a cada intervalo de tempo nas diferentes áreas do sistema.
 
---
 
### Exercícios — Appliances Energy Prediction
 
| Item | Detalhe |
|------|---------|
| Fonte | UCI Machine Learning Repository |
| Link | https://archive.ics.uci.edu/dataset/374/appliances+energy+prediction |
| Arquivo principal | `energydata_complete.csv` |
| Período original | 4,5 meses (2016), medições a cada 10 minutos |
| Total de registros | ~19.735 |
| Variáveis principais | Consumo de eletrodomésticos (Wh), temperatura e umidade de 9 cômodos |
 
O dataset foi coletado em uma casa de baixo consumo energético na Bélgica. As medições incluem o consumo dos eletrodomésticos, o consumo de iluminação e variáveis climáticas internas e externas, tornando-o ideal para análise de eficiência energética residencial.
 
---
 
##  Tecnologias Utilizadas
 
| Ferramenta | Uso |
|------------|-----|
| Python 3 | Linguagem principal |
| Pandas | Manipulação e análise de dados |
| Matplotlib | Geração de gráficos |
| Requests | Consulta à API do ONS |
| Orange Data Mining | Preparação visual dos dados (Etapa A dos exercícios) |
| Jupyter Notebook | Ambiente de desenvolvimento dos notebooks |
 
### Instalação das dependências
 
```bash
pip install pandas matplotlib requests seaborn
```
 
---
 
##  Como Executar
 
### Desafio Final
1. Abra `desafio_final.ipynb` no Jupyter ou Google Colab
2. Execute todas as células em ordem
3. A API é consultada automaticamente — nenhum arquivo externo é necessário
### Exercícios (Aulas 03 e 04)
1. Baixe o dataset em: https://archive.ics.uci.edu/dataset/374/appliances+energy+prediction
2. Abra o arquivo `energydata_complete.csv` no **Orange Data Mining**
3. Siga a Etapa A descrita no notebook para preparar e exportar `amostra.csv`
4. Coloque `amostra.csv` na mesma pasta que `exercicios_aulas_03_04.ipynb`
5. Execute todas as células do notebook
---
 
##  Integrantes do Grupo
 
| Nome | RM |
|------|----|
| (Gabriel de Oliveira Souza) | (571583) |
| (João Melo) | (571116) |
| (Rafael Sá) | (569223) |
---
 
