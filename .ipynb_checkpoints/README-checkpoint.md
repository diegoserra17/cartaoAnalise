# Análise de Cartão de Crédito x Risco de Inadimplência
Um exercício sobre o problema de uma empresa de cartão de crédito, com um dataset de dados demográficos e financeiros dos últimos 6 meses (amostra de 30.000 linhas). Os dados estão em um nível de conta de crédito, ou seja, cada linha é uma conta.
As linhas são rotuladas de acordo como se no mês seguinte ao período de dados histórico de seis meses um proprietário da conta ficou inadimplente, ou seja, não fês o pagamento mínimo.

## O objetivo
O objetivo é desenvolver um modelo que preveja, de acordo com o padrão dos dados históricos, se uma conta ficará inadimplente no próximo mês.


## Exploração
1. Quantas colunas os dados tem?
2. Quantas amostras (linhas)
3. Que tipos de caracteristicas existem. Quais são os dados Categóricos e Numéricos?
4. Qual é a aparência dos dados segundo essas características?
5. Há dados faltando?
Vamos usar o Pandas para verificar a integridade básica dos dados.

## Informações dos dados
- LIMIT_BAL - Valor do Crédito Fornecido (dólares taiwaneses) inclusive o crédito do consumidor individual e familiar;
- SEX - Gênero (1=Masculino; 2=Feminino);
- EDUCATION - Instrução (1=Pós-Graduação; 2=Universidade; 3=Ensino Médio; 4=Outros)
- MARRIAGE - (1=casado; 2=Solteiro; 3=Outros)
- AGE - Idade (ano)

  **PAY_1 a PAY_6 - Registro de pagamentos passados.Mensais de abril a setembro são armazenados nessas colunas:**
- PAY_1 - setembro
- PAY_2 - agosto
- PAY_3 - julho
- PAY_4 - junho
- PAY_5 - maio
- PAY_6 - abril
  *A escala de medida do status de reembolso é a seguinte: -1 =Pagamento Pontual; 1 = atraso de um mês; 2 = atraso de 2 meses... e assim por diante até o 9 = nome meses de atraso ou mais.*

  **BILL_AMT1 a BILL_AMT6 - Valor da fatura (em dólares taiwaneses):**
- BILL_AMT1 - setembro
- BILL_AMT2 - agosto
- BILL_AMT3 - julho
- BILL_AMT4 - junho
- BILL_AMT5 - maio
- BILL_AMT6 - abril
