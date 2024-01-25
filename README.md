# Alocação e Otimização de Portfólios

Claro, aqui está um texto em formato markdown para adicionar ao seu repositório no GitHub para o script fornecido:

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

O resultado final da alocação aleatória é apresentado no DataFrame `dataset`, onde cada linha representa o valor investido em cada ação ao longo do tempo, a taxa de retorno diária e a soma total do valor investido.

Este script faz parte do curso de Análise de Dados com Python, ministrado pelo professor Jonas, através da plataforma Udemy, e aborda temas de relevância acadêmica na área de finanças.

Se precisar de mais informações ou esclarecimentos, sinta-se à vontade para entrar em contato!
```

Certifique-se de ajustar o texto conforme necessário e adicionar informações adicionais que julgar relevantes para o contexto do seu repositório no GitHub.