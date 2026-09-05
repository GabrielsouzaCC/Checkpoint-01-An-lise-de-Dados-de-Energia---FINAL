# ⚡ Análise de Dados de Energia — SERS / FIAP

**Curso:** Ciência da Computação  
**Disciplina:** Soluções em Energias Renováveis e Sustentáveis  
**Instituição:** FIAP  

---

## 📋 Sobre o Projeto

Este repositório reúne as atividades práticas de análise de dados do setor de energia elétrica desenvolvidas nas aulas 03, 04 e como desafio final da disciplina de Soluções em Energias Renováveis e Sustentáveis (SERS).

O objetivo geral é aplicar técnicas de preparação, manipulação e interpretação de dados reais do setor energético utilizando **Python**, **Pandas**, **Matplotlib** e **Orange Data Mining**, sem o uso de modelos de aprendizado de máquina — o foco está na análise exploratória e nos indicadores estatísticos.

---

## 📁 Estrutura do Repositório

```
📦 analise-dados-energia-sers
 ┣ 📓 desafio_final.ipynb          ← Desafio Final: API pública do ONS
 ┣ 📓 exercicios_aulas_03_04.ipynb ← Exercícios das Aulas 03 e 04 (6 datasets)
 ┗ 📄 README.md                    ← Este arquivo
```

---

## 📂 Descrição dos Arquivos

### 📓 `desafio_final.ipynb`

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

### 📓 `exercicios_aulas_03_04.ipynb`

Notebook com a resolução dos exercícios práticos das aulas 03 e 04, cobrindo os **6 datasets** da disciplina. Para cada dataset o notebook contém a descrição da Etapa A (Orange Data Mining) e a resolução completa da Etapa B (Python / Pandas).

| # | Dataset | Fonte | Arquivo da amostra | Limiar | Segundo critério |
|---|---------|-------|--------------------|--------|-----------------|
| 1 | Appliances Energy Prediction | UCI | `amostra_ds1.csv` | 70% do máximo | Alto consumo + temperatura acima da média |
| 2 | Steel Industry Energy Consumption | UCI | `amostra_ds2.csv` | 75% do máximo | Alto consumo + fator de potência abaixo de 0,85 |
| 3 | Power Consumption of Tetouan City | UCI | `amostra_ds3.csv` | 70% do pico da zona | Consumo alto + temperatura acima da média |
| 4 | Solar Power Generation Data | Kaggle | `amostra_ds4.csv` | 80% da geração AC | Alta geração AC + geração diária acima da média |
| 5 | Wind & Solar Energy Production | Kaggle | `amostra_ds5.csv` | 80% de cada fonte | Alta produção eólica E solar simultaneamente |
| 6 | Individual Household Power Consumption | UCI | `amostra_ds6.csv` | 75% da potência ativa | Alta potência + climatização acima da média |

> ⚠️ O Dataset 6 usa `;` como separador de colunas e `?` para valores ausentes. O código já trata isso automaticamente.

---

## 🗂️ Fontes dos Dados

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

### Exercícios — Datasets das Aulas 03 e 04

| # | Dataset | Fonte | Link |
|---|---------|-------|------|
| 1 | Appliances Energy Prediction | UCI | https://archive.ics.uci.edu/dataset/374/appliances+energy+prediction |
| 2 | Steel Industry Energy Consumption | UCI | https://archive.ics.uci.edu/dataset/851/steel+industry+energy+consumption |
| 3 | Power Consumption of Tetouan City | UCI | https://archive.ics.uci.edu/dataset/849/power+consumption+of+tetouan+city |
| 4 | Solar Power Generation Data | Kaggle | https://www.kaggle.com/datasets/anikannal/solar-power-generation-data |
| 5 | Wind & Solar Energy Production | Kaggle | https://www.kaggle.com/datasets/ramyakmurthy/wind-and-solar-energy-production-dataset |
| 6 | Individual Household Power Consumption | UCI | https://archive.ics.uci.edu/dataset/235/individual+household+electric+power+consumption |

---

## 🛠️ Tecnologias Utilizadas

| Ferramenta | Uso |
|------------|-----|
| Python 3 | Linguagem principal |
| Pandas | Manipulação e análise de dados |
| Matplotlib | Geração de gráficos |
| Requests | Consulta à API do ONS |
| Orange Data Mining | Preparação visual dos dados (Etapa A dos exercícios) |
| Jupyter Notebook | Ambiente de desenvolvimento |

### Instalação das dependências

```bash
pip install pandas matplotlib requests
```

---

## ▶️ Como Executar

### Desafio Final
1. Abra `desafio_final.ipynb` no Jupyter ou Google Colab
2. Execute todas as células em ordem
3. A API é consultada automaticamente — nenhum arquivo externo é necessário

### Exercícios (Aulas 03 e 04)
1. Baixe o dataset correspondente no link da tabela acima
2. Abra o arquivo no **Orange Data Mining** e siga a Etapa A descrita no notebook
3. Exporte a amostra com o nome correto (`amostra_ds1.csv`, `amostra_ds2.csv`, etc.)
4. Coloque o arquivo exportado na mesma pasta que `exercicios_aulas_03_04.ipynb`
5. Execute as células do dataset correspondente ao seu grupo

---

## 👥 Integrantes do Grupo

| Nome | RM |
|------|----|
| (preencher) | (preencher) |
| (preencher) | (preencher) |

---

## 📅 Entrega

- **Apresentação:** Aula 05 — 04/09
- **Envio:** link deste repositório pelo botão Anexar na tarefa
