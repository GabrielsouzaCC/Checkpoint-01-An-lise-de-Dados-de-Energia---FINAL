# Análise de Dados de Energia — SERS / FIAP

**Curso:** Ciência da Computação  
**Disciplina:** Soluções em Energias Renováveis e Sustentáveis  

---

## Descrição

Repositório com as atividades práticas de análise de dados do setor de energia, desenvolvidas nas aulas 03, 04 e como desafio final da disciplina.

---

## Arquivos

| Arquivo | Descrição |
|---|---|
| `desafio_final.ipynb` | Desafio Final — análise da carga elétrica de SP via API pública do ONS |
| `exercicios_aulas_03_04.ipynb` | Exercícios das aulas 03 e 04 — Dataset: Appliances Energy Prediction (UCI) |

---

## Fontes dos Dados

### Desafio Final — API ONS (Operador Nacional do Sistema Elétrico)
- **Portal:** https://dados.ons.org.br/
- **Dataset:** Carga Verificada do ONS
- **Endpoint:** https://apicarga.ons.org.br/prd/cargaverificada
- **Região:** SP — São Paulo
- **Período:** 01/08/2025 a 07/08/2025

### Exercícios — Appliances Energy Prediction
- **Fonte:** UCI Machine Learning Repository
- **Link:** https://archive.ics.uci.edu/dataset/374/appliances+energy+prediction
- **Descrição:** Consumo de eletrodomésticos em residência de baixo consumo, com variáveis de temperatura e umidade coletadas a cada 10 minutos.

---

## Bibliotecas Utilizadas

```
requests
pandas
matplotlib
seaborn
```

Instalar com:
```
pip install requests pandas matplotlib seaborn
```
