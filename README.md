# Classificação de Dígitos Manuscritos com Machine Learning

## Link do vídeo

- Vídeo: [insira o link do vídeo]

## Clone do repositório

```bash
git clone [insira o link do repositório]
```

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

### 1) Execução local (recomendado para desenvolvimento)

1. Crie e ative um ambiente virtual Python com Python 3.11 ou 3.12.
2. Instale as dependências:

   ```bash
   python -m venv .venv
   .venv\Scripts\activate
   pip install -r requirements.txt
   ```

3. Abra o arquivo `main.ipynb` no Jupyter Notebook ou no VS Code.
4. Execute as células em ordem, da Fase 1 até a Fase 5.
5. Para a Fase 5.3, mantenha uma imagem `.png` ou `.jpeg` dentro da pasta
   `imagem`.

> Se o ambiente apresentar erro relacionado a `np.long` ou importação do
> SciPy/Scikit-learn, reinstale as bibliotecas com versões compatíveis:
>
> ```bash
> pip install -U "numpy>=2.0,<2.8" "scipy>=1.14.1" "scikit-learn>=1.5.2"
> ```

### 2) Execução no Google Colab

1. Abra o notebook no Colab ou carregue o projeto no Google Drive.
2. Monte o Drive:

   ```python
   from google.colab import drive
   drive.mount('/content/drive')
   %cd /content/drive/MyDrive/Modulo-02-MniProjeto
   ```

3. Instale as dependências compatíveis:

   ```python
   !pip install -q -U pip
   !pip install -q "numpy>=2.0,<2.8" "scipy>=1.14.1" "scikit-learn>=1.5.2" \
                   "pandas>=2.2" "matplotlib>=3.8" "seaborn>=0.13" \
                   "opencv-python>=4.9" "tensorflow>=2.15"
   ```

4. Verifique se o ambiente está funcionando:

   ```python
   import numpy as np
   import scipy
   import sklearn
   import tensorflow as tf
   from tensorflow import keras

   print(np.__version__)
   print(scipy.__version__)
   print(sklearn.__version__)
   print(tf.__version__)
   print(keras.__version__)
   ```

5. Crie ou use a pasta da imagem:

   ```python
   !mkdir -p /content/imagem
   ```

6. Execute as células em ordem, da Fase 1 até a Fase 5.

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

## Observação importante sobre compatibilidade

Para evitar o erro `AttributeError: module 'numpy' has no attribute 'long'`,
use versões compatíveis de NumPy, SciPy e scikit-learn. O Colab normalmente
funciona corretamente com estas versões:

- NumPy: `>=2.0,<2.8`
- SciPy: `>=1.14.1`
- scikit-learn: `>=1.5.2`

## Possíveis melhorias

- Ajustar hiperparâmetros com validação cruzada.
- Avaliar uma rede convolucional (CNN).
- Testar mais imagens manuscritas e diferentes condições de iluminação.
- Criar uma interface simples para envio de imagens.
