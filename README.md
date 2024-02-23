# Modelagem de banco de dados para análise preditiva de máquinas

O presente projeto possui o objetivo de fazer uma modelagem de banco de dados para abrigar dados de manutenção preditiva de máquinas, a fim de resolver problemas de negócio. Os dados foram retirados do [Kaggle](https://www.kaggle.com/datasets/arnabbiswas1/microsoft-azure-predictive-maintenance). 

<b> Telemetry Time Series Data (PdM_telemetry.csv)</b>: Dados de Séries Temporais de Telemetria (PdM_telemetry.csv): Consiste na média horária de voltagem, rotação, pressão e vibração coletados de 100 máquinas durante o ano de 2015.

<h3>Dados e Contexto:</h3>

<b>Error (PdM_errors.csv)</b>: Estes são erros encontrados pelas máquinas durante a operação. Como esses erros não desligam as máquinas, eles não são considerados como falhas. As datas e horários dos erros são arredondados para a hora mais próxima, já que os dados de telemetria são coletados a cada hora.

<b>Maintenance (PdM_maint.csv)</b>: Se um componente de uma máquina é substituído, isso é capturado como um registro nesta tabela. Os componentes são substituídos em duas situações: 1. Durante a visita regular programada, o técnico o substituiu (Manutenção Proativa) 2. Um componente quebra e então o técnico faz uma manutenção não programada para substituir o componente (Manutenção Reativa). Isso é considerado como uma falha e os dados correspondentes são capturados sob Falhas. Os dados de manutenção têm registros tanto de 2014 quanto de 2015. Esses dados são arredondados para a hora mais próxima, já que os dados de telemetria são coletados a cada hora.

<b>Failures (PdM_failures.csv)</b>: Cada registro representa a substituição de um componente devido a uma falha. Estes dados são um subconjunto dos dados de Manutenção. Estes dados são arredondados para a hora mais próxima, já que os dados de telemetria são coletados a cada hora.

<b>Metadata of Machines (PdM_Machines.csv)</b>: Tipo de modelo e idade das Máquinas.

<h3>Perguntas de negócio para querys:</h3>

1. Qual modelo de máquina apresenta mais falhas. <br>
2. Qual a quantidade de falhas por idade da máquina. <br>
3. Qual componente apresenta maior quantidade de falhas por máquina.<br>
4. A média da idade das máquinas por modelo.<br>
5. Quantidade de erro por tipo de erro e modelo da máquina.<br>

