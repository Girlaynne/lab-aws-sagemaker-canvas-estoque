# 📊 Previsão de Estoque Inteligente na AWS com [SageMaker Canvas](https://aws.amazon.com/pt/sagemaker/canvas/)

Desafio de Projeto:
Projeto de criação de um Modelo baseado em Machine Learning No-Code para uma "Previsão de Estoque Inteligente" com o uso do SageMaker Canvas na AWS.

## 🎯 Objetivos Deste Desafio de Projeto (Lab)

![image](https://github.com/digitalinnovationone/lab-aws-sagemaker-canvas-estoque/assets/730492/72f5c21f-5562-491e-aa42-2885a3184650)

## 🚀 Passo a Passo

### 1. Selecionar Dataset

É preciso escolher o dataset para treinar o modelo de previsão de estoque. Escolhi o dataset-1000-com-preco-promocional-e-renovacao-estoque.csv, disponível na pasta datasets.

### 2. Construir/Treinar

Criei um novo modelo e selecionei Predictive Analysis para fazer previsões através de dados. Após fazer o upload do dataset escolhido, selecionei a coluna QUANTIDADE_ESTOQUE para o modelo prever. Em Configure Model, selecionei a coluna ID_PRODUTO para identificar os itens da coluna QUANTIDADE_ESTOQUE e iniciei o treinamento do modelo.

### 3. Analisar

Após o treinamento, obtive as seguintes métricas, sabendo que quanto menor a métrica melhor o resultado:
- Avg.wQL - 0.060 - Avg. wQL (Média da Perda Quantil Ponderada): Essa métrica mede o erro nas previsões, ponderado pela importância de cada item.
- MAPE - 0.148 - (Erro Percentual Médio Absoluto): Calcula a média da porcentagem de erro das previsões em relação aos valores reais.
- WAPE - 0.100 - (Erro Percentual Absoluto Ponderado): Similar ao MAPE, mas leva em consideração a importância de cada item no estoque. Isso significa que itens de maior valor ou importância terão um impacto maior na métrica.
- RMSE - 5.765 - (Raiz do Erro Quadrático Médio): Mede a diferença média entre os valores previstos e os valores reais, dando mais peso a grandes erros.
- MASE - 0.301 - Erro Escalado Médio Absoluto): Compara o erro da previsão com um modelo simples. 
A coluna que teve um maior impacto foi PRECO. 

### 4. Prever

É possível ver a previsão de cada item.
- P10 (10º Percentil): Representa um valor abaixo do qual 10% das previsões estão.
- P50 (50º Percentil): Este é o valor mediano nas previsões, mostrando a demanda média esperada.
- P90 (90º Percentil): Indica um valor acima do qual 10% das previsões estão.
