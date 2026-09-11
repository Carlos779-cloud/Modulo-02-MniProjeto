# Classificação de Dígitos Manuscritos com Machine Learning

Mini-projeto avaliativo do Módulo 2. O projeto compara modelos de Machine
Learning para classificar imagens de dígitos manuscritos do conjunto de dados
MNIST.

## Objetivo

Treinar e avaliar modelos como Random Forest, KNN, SVM e MLP, considerando
acurácia, precisão, recall, F1-score e tempo de treinamento. O notebook também
analisa o comportamento de um modelo diante de classes que não aparecem no
conjunto de treino e realiza inferência em uma imagem manuscrita própria.

## Tecnologias

- Python
- Pandas e NumPy
- Scikit-learn
- Matplotlib e Seaborn
- OpenCV
- Jupyter Notebook

## Estrutura

```text
main.ipynb              # desenvolvimento completo do projeto
requirements.txt        # dependências Python
imagem/                 # imagem manuscrita usada na Fase 5.3
outputs/graficos/       # gráficos gerados pelo notebook
data/                   # cache local do MNIST, criado automaticamente
```

## Como executar

1. Crie e ative um ambiente virtual Python.
2. Instale as dependências:

   ```bash
   pip install -r requirements.txt
   ```

3. Abra o arquivo `main.ipynb` no Jupyter Notebook ou no VS Code.
4. Execute as células em ordem, da Fase 1 até a Fase 5.
5. Para a Fase 5.3, mantenha uma imagem `.jpg` ou `.jpeg` dentro da pasta
   `imagem`.

No Google Colab, envie a imagem para `/content/imagem` antes de executar a
Fase 5.3.

## Execução local e Google Colab

O notebook possui a variável `AMBIENTE` antes da célula do SVM:

- `AMBIENTE = "local"`: usa uma amostra estratificada de 12.000 imagens no
  SVM e desativa a calibração de probabilidades desse modelo. Esse é o perfil
  usado para desenvolvimento e testes rápidos no computador.
- `AMBIENTE = "colab"`: usa todas as imagens de treinamento e probabilidades
  calibradas. Este perfil é recomendado para a execução final e para registrar
  os resultados do projeto.

O SVM com kernel RBF não usa GPU automaticamente no scikit-learn; a diferença
na velocidade no Colab normalmente vem da CPU, da memória e das bibliotecas
numéricas. Ao apresentar os resultados, informe o perfil utilizado, pois tempos
 e acurácia do SVM podem variar entre eles.

## Possíveis melhorias

- Ajustar hiperparâmetros com validação cruzada.
- Avaliar uma rede convolucional (CNN).
- Testar mais imagens manuscritas e diferentes condições de iluminação.
- Criar uma interface simples para envio de imagens.
