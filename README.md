# Alocação e Otimização de Portfólios


```markdown
# Curso de Análise de Dados com Python

## Python para Finanças - Alocação e Otimização de Portfólios

### Importação das bibliotecas e base de dados

```python
import pandas as pd 
import numpy as np 
import matplotlib.pyplot as plt 
import plotly.express as px 

dataset = pd.read_csv('acoes2.csv')
```

O conjunto de dados `acoes2.csv` contém informações sobre ações, incluindo os preços diários de ações de diferentes empresas.

### Alocação Aleatória de Ativos

A alocação aleatória de ativos é uma técnica para distribuir um capital entre diferentes ativos de maneira aleatória. O código abaixo realiza essa alocação para as ações no conjunto de dados.

```python
# Função para alocar ativos aleatoriamente
def alocacao_ativos(dataset, dinheiro_total, seed=0):
    # ... (código da função)
    return dataset, datas, acoes_pesos, dataset.loc[len(dataset) - 1]['Soma valor']

# Chamando a função
dataset, datas, acoes_pesos, soma_valor = alocacao_ativos(pd.read_csv('acoes2.csv'), 5000, 10)
```

A função `alocacao_ativos` recebe o conjunto de dados, o capital total a ser investido e uma semente para a geração de números aleatórios. Ela aloca o capital de forma aleatória entre as ações e calcula a taxa de retorno ao longo do tempo.

### Resultados da Alocação

O resultado da alocação é armazenado no DataFrame `dataset`, que inclui a soma do valor investido em todas as ações e a taxa de retorno diária. Além disso, as datas e os pesos atribuídos a cada ação são armazenados em `datas` e `acoes_pesos`, respectivamente.

```python
# Exibindo resultados
print(dataset)
print(datas)
print(acoes_pesos)
print(soma_valor)
```

### Métricas de Desempenho do Portfólio

Vamos calcular algumas métricas adicionais para avaliar o desempenho do portfólio:

- Retorno acumulado em todo o período:

```python
retorno_acumulado = dataset.loc[len(dataset) - 1]['Soma valor'] / dataset.loc[0]['Soma valor'] - 1
print(retorno_acumulado)
```

- Desvio padrão (risco da carteira):

```python
risco_carteira = dataset['Taxa retorno'].std()
print(risco_carteira)
```

- Sharpe ratio médio anual (sem considerar a taxa SELIC):

```python
sharpe_ratio = (dataset['Taxa retorno'].mean() / risco_carteira) * np.sqrt(246)
print(sharpe_ratio)
```
Lembre-se de que um Sharpe ratio maior indica um desempenho melhor, e valores acima de 1.0 são considerados aceitáveis.

### Rendimento em Investimento de Renda Fixa

Finalmente, calculamos o rendimento adquirido em um investimento de renda fixa, considerando a taxa SELIC histórica.

```python
rendimentos_fixos = valor_2020 - dinheiro_total
ir = rendimentos_fixos * 15 / 100  # Desconto do Imposto de Renda
valor_liquido_total = valor_2020 - ir
print(rendimentos_fixos)
print(ir)
print(valor_liquido_total)
```

*Obs.: Lembre-se de ajustar as taxas SELIC de acordo com o ano desejado.*

O resultado final da alocação aleatória é apresentado no DataFrame `dataset`, onde cada linha representa o valor investido em cada ação ao longo do tempo, a taxa de retorno diária e a soma total do valor investido.

Este script faz parte do curso de Análise de Dados com Python, ministrado pelo professor Jonas, através da plataforma Udemy, e aborda temas de relevância acadêmica na área de finanças.

## Recursos

[Link para o Curso na Udemy](https://www.udemy.com/course/python-para-financas-analise-de-dados-e-machine-learning/learn/lecture/23802824#overview)

[Professor Jones - IA Expert Academy](https://www.linkedin.com/school/ia-expert-academy/)

Lembre-se de manter a integridade dos dados e aproveite a exploração dos conceitos de análise de dados em Python aplicados a portfólios de ações.


