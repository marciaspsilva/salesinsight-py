# SalesInsight PY

## Sobre o projeto

O **SalesInsight PY** é um projeto de análise de dados de vendas desenvolvido em Python com o objetivo de demonstrar o conhecimento adquirido no curso de Desenvolvimento de IA para análise preditiva [T4].

O projeto realiza o carregamento, inspeção, limpeza, transformação e análise de um dataset de vendas, gerando métricas por período, produto, categoria e região, além de uma segmentação de clientes por faixa de gasto.

O fluxo foi organizado em funções reutilizáveis e inclui uma função de ordem superior, demonstrando a aplicação de funções como argumento.

## O que o projeto analisa

* Receita total e volume de vendas por mês
* Quantidade e número de vendas por período
* Top 5 produtos por receita
* Receita total por categoria
* Receita total e ticket médio por região
* Segmentação de clientes por nível de gasto:

  * Bronze
  * Prata
  * Ouro
* Criação de colunas derivadas para análise dos dados
* Exportação dos resultados em CSV e JSON

## Requisitos Funcionais

### RF01 – Criar ou carregar o dataset de vendas
Geração e leitura do dataset de vendas em formato CSV.

### RF02 e RF03 – Inspecionar e tratar os dados
Inspeção da estrutura dos registros, identificação de dados inconsistentes e tratamento dos registros conforme as regras definidas para o projeto.

### RF04 – Criar colunas derivadas com transformações condicionais
Criação de novas colunas a partir dos dados existentes, incluindo transformações condicionais e informações derivadas das datas e da receita.

### RF05 – Calcular métricas agregadas por Mês, Produto, Categoria e Região
Cálculo de métricas agregadas por:

* Mês
* Produto
* Categoria
* Região

### RF06 – Segmentar clientes por nível de gasto

Agrupamento dos clientes pelo total gasto e classificação em segmentos:

* Bronze
* Prata
* Ouro

### RF07 – Organizar o código em funções reutilizáveis

Organização do fluxo em funções com parâmetros, retorno e docstrings.

O projeto também implementa uma função de ordem superior que recebe uma função de transformação como argumento e a aplica aos valores de uma coluna dos registros.

### RF08 – Exportar resultados em CSV e JSON

Exportação dos resultados das análises em arquivos CSV e JSON.

## Conceitos aplicados

**Módulo 01 – Semanas 01 a 05**

* Lógica de programação
* Variáveis, tipos e operadores
* Estruturas condicionais
* Listas, tuplas, dicionários e estruturas compostas
* Funções com parâmetros e retorno
* Docstrings
* Funções lambda
* Funções de ordem superior
* Leitura e escrita de arquivos CSV
* Leitura e escrita de arquivos JSON
* Módulo `datetime`
* Expressões regulares com `re`
* Organização do código em funções reutilizáveis
* Git e GitHub
* Branches e commits
* GitFlow simplificado

## Como executar

### Google Colab

Para executar o projeto pelo Google Colab:

1. Faça upload dos arquivos `salesinsight.py` e `vendas.csv`.
2. Execute:

```python
!python salesinsight.py
```

Também é possível utilizar o código em um notebook `.ipynb`, executando as funções nas células e, ao final, a função `main()`.

### Localmente com VS Code

1. Instale o Python 3.10 ou superior.
2. Abra o projeto no VS Code.
3. Não é necessária a instalação de dependências externas, pois o projeto utiliza apenas bibliotecas da biblioteca padrão do Python.
4. Execute no terminal:

```bash
python salesinsight.py
```

## Estrutura do projeto

```text
salesinsight-py/
│
├── salesinsight.py
├── vendas.csv
├── README.md
│
├── exportacao-resultados/
│   ├── metricas_por_mes.csv
│   ├── segmentacao_clientes.csv
│   └── segmentacao_clientes.json

```

O arquivo `salesinsight.py` contém o fluxo principal do projeto.

O notebook `salesinsights.ipynb` permite executar e acompanhar as etapas do projeto de forma interativa no Google Colab.

A pasta `exportacao-resultados` contém os arquivos gerados pela etapa de exportação dos resultados.

## Ponto de entrada

O projeto possui uma função `main()` responsável por executar o fluxo completo.

A função verifica a existência do dataset, executa as etapas de carregamento, inspeção, tratamento, transformação, cálculo das métricas, segmentação dos clientes e exportação dos resultados.

A execução do arquivo `salesinsight.py` utiliza:

```python
if __name__ == "__main__":
    main()
```

Dessa forma, o fluxo completo pode ser executado diretamente pelo arquivo Python.

## Exportação dos resultados

Os resultados são armazenados na pasta:

```text
exportacao-resultados/
```

Os arquivos gerados incluem:

* `metricas_por_mes.csv` — métricas agregadas por mês.
* `segmentacao_clientes.csv` — clientes classificados por segmento.
* `segmentacao_clientes.json` — dados de segmentação armazenados em formato JSON.

## Ferramentas utilizadas

* Python 3.10+
* Google Colab
* Visual Studio Code
* Git
* GitHub

### Bibliotecas utilizadas

O projeto utiliza somente bibliotecas da biblioteca padrão do Python:

* `csv`
* `json`
* `re`
* `datetime`
* `os`
* `random`

## Versionamento

O projeto utiliza Git e GitHub para controle de versão.

## Vídeo de demonstração

INSERIR AQUI O LINK DO VÍDEO
