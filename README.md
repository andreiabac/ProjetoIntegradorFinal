# ProjetoIntegradorFinal

Predição do Faturamento de uma distribuidora de Implementos Médicos e Medicamentos

Objetivo
  O objetivo do Projeto é criar modelos de  predição do faturamento de uma distribuidora de Implementos Médicos e Medicamentos buscando prever o Faturamento para o próximo Ano.
  
Sobre os dados e análise exploratória.
  Os modelos foram testados a fim de prever 1 ano (12 meses) do faturamento das notas fiscais.
  Os dados são controlados e gerados por um sistema ERP e estão dentro de um Banco de Dados geridos por um SGDB.
  As features encontradas se referem a itens de notas fiscais de faturamento.
  A  base de dados possui informações desde 2008 até a data atual, somando no total 164.959.
  O faturamento será estimado utilizando o valor total das vendas obtido com a informação da feature “valor”.
   EAD Transformação dos Dados:
      -Transformação da feature “valor” para float.
      -Transformação das features “ano” e "mês" para string.
      -Criação de uma nova coluna DATA concatenando a feature "mês" e “ano” e convertendo para datetime.
      -Agrupamento das datas com a soma do valor total de vendas e definição do índice por DATA.
      -Criação do data frame de vendas ano a partir do agrupamento, foi utilizada a função resample, levando a série para um espaço de tempo maior, passamos de dias para meses.
      -E com a função mean() agrupamos todas as vendas do mês e calculamos a média.
      
Modelos testados:
    1 - Tendência Linear
    2 - Tendência quadrática
    3 - Tendência com transformação logarítmica
    4 - Single Exponential Smoothing (suavização exponencial simples)
    5 - Triple Exponential Smoothing
    6 - ARIMA
    7 - SARIMA
    8 - Prophet
    9 - Xgboost
    10 - LSTM Rede Neural Profunda
    11 - Ensemble
