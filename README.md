# IC - Análise de Séries Temporais do Porto de Santos com Lógica Fuzzy

Este repositório contém o código e os dados utilizados na Iniciação Científica "Proposta de Aplicação de Lógica Fuzzy em Séries Temporais no Porto de Santos", do curso de Ciência de Dados da FATEC-RL.

## Objetivo do Projeto

O objetivo principal deste trabalho é explorar a aplicação de conceitos de Lógica Fuzzy (como o `scikit-fuzzy` e `pyFTS`) para analisar e, eventualmente, prever a movimentação de cargas (em toneladas) no Porto de Santos.

## Estrutura do Repositório

* **/dados/**
    * `exportacao_cargas.csv`: O conjunto de dados brutos extraído do Mensário Estatístico do Porto de Santos, contendo a movimentação de cargas de 2013 a 2023.
* **/outputs/**
    * `serietemporal.csv`: O conjunto de dados tratado, agregado mensalmente de 2019 a 2023, que serve como entrada para os modelos de séries temporais.
* `ETL.ipynb`: Jupyter Notebook contendo todo o processo de ETL (Extração, Transformação e Carga), que converte os dados brutos (`exportacao_cargas.csv`) na série temporal final (`serietemporal.csv`).
* `Analise_Fuzzy.ipynb`: (Previsão para o seu próximo arquivo) Notebook principal contendo a análise e modelagem Fuzzy.

## Executando o Projeto

### 1. Pré-requisitos

O projeto foi desenvolvido em Python 3. Você precisará das seguintes bibliotecas:

```bash
pip install pandas
```

### 2. Executando o ETL

Para gerar a série temporal tratada, basta executar o notebook `ETL.ipynb`. Ele irá:
1.  Carregar os dados brutos de `/dados/exportacao_cargas.csv`.
2.  Limpar, filtrar e agregar os dados.
3.  Salvar a série temporal final em `/outputs/serietemporal.csv`.

## 📊 Fonte dos Dados

Os dados brutos foram extraídos do [Mensário Estatístico do Porto de Santos](http://mensario.portodesantos.com.br/cargas/).

O processo de ETL foi inspirado e adaptado do trabalho de Renato Campos, disponível em [seu repositório sobre o PI3 do Porto de Santos](https://github.com/renato-campos/pi3-porto-de-santos.git).
