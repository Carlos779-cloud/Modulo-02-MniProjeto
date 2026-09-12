# Conclusão do Projeto

## Visão geral

Este projeto teve como objetivo desenvolver e comparar modelos de Machine Learning para reconhecer dígitos manuscritos do conjunto MNIST. A análise abrangeu diferentes abordagens supervisionadas, com foco em desempenho preditivo, custo computacional e capacidade de generalização. O processo foi realizado a partir da exploração do dataset, do treinamento dos modelos e da avaliação com métricas como acurácia, precisão, recall, F1-score e tempo de treinamento.

## Principais resultados

Os modelos avaliados foram: Random Forest, KNN, SVM, MLP e uma rede neural em Keras. Os resultados mostraram que a arquitetura baseada em redes neurais conseguiu o melhor desempenho geral, enquanto o SVM apresentou um equilíbrio muito interessante entre qualidade de classificação e robustez. Em termos de acurácia no conjunto de teste, os principais resultados foram:

- Rede Neural (Keras): 98,10%
- SVM: 97,74%
- MLP: 97,69%
- KNN: 97,07%
- Random Forest: 94,44%

Esses valores demonstram que o problema de classificação dos dígitos manuscritos foi resolvido com alto nível de precisão pelos modelos mais sofisticados, especialmente os que aprendem representações mais complexas dos dados.

## Interpretação dos resultados

A rede neural em Keras obteve o melhor desempenho, o que reforça a ideia de que modelos mais flexíveis e com maior capacidade de aprendizado conseguem capturar melhor as nuances entre os dígitos. O SVM, por sua vez, mostrou ser uma alternativa extremamente competitiva, especialmente em tarefas de classificação com padrões bem definidos como o MNIST. Já o KNN apresentou desempenho bom, porém mais sensível ao espaço de características e ao custo de memória e inferência, além de depender mais diretamente da similaridade entre amostras.

O Random Forest, embora tenha alcançado uma boa taxa de acerto, ficou atrás dos demais. Isso indica que árvores de decisão, apesar de serem úteis e interpretáveis, não são tão eficazes quanto modelos dedicados ao aprendizado de padrões em imagens de alta dimensionalidade.

## Aprendizados do projeto

Além dos resultados quantitativos, o projeto também evidenciou aspectos importantes do processo de desenvolvimento em Aprendizado de Máquina:

- a qualidade dos dados e o pré-processamento influenciam diretamente o desempenho;
- modelos distintos têm custos computacionais e comportamentos diferentes;
- o equilíbrio entre acurácia e eficiência deve ser considerado na escolha final do algoritmo;
- modelos de alto desempenho exigem atenção a hiperparâmetros, validação e tempo de treinamento;
- a avaliação qualitativa das previsões é essencial para identificar erros concentrados em classes específicas.

## Conclusão final

Conclui-se que o projeto cumpriu com sucesso o objetivo de comparar modelos de classificação para dígitos manuscritos, mostrando claramente que a escolha do algoritmo impacta diretamente o desempenho final. O modelo em Keras foi o mais preciso, enquanto o SVM se mostrou uma excelente alternativa em termos de qualidade e eficiência. Em conjunto, os resultados evidenciam que a classificação de imagens do MNIST pode ser resolvida de forma altamente eficiente com técnicas clássicas e modernas de Machine Learning.

Esse trabalho também reforça a importância da experimentação e da comparação crítica entre modelos, pois a melhor solução não depende apenas de acurácia, mas também do contexto de uso, do custo computacional e da escalabilidade do sistema.
