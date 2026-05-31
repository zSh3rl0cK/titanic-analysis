# 🚢 Titanic Analysis

Análise Exploratória de Dados (EDA) e modelagem preditiva sobre o clássico dataset do Titanic, desenvolvido como exercício prático da disciplina de Inteligência Artificial do curso de Engenharia de Software.

---

## 📋 Sobre o Projeto

O objetivo deste projeto é realizar uma análise completa sobre os dados dos passageiros do Titanic, passando por todas as etapas fundamentais de um projeto de Machine Learning:

- Inspeção e compreensão dos dados brutos
- Classificação e tratamento de variáveis
- Identificação e tratamento de valores faltantes
- Detecção e análise de outliers
- Visualização de distribuições e correlações
- Análise comparativa entre grupos
- *(Em desenvolvimento)* Construção e avaliação de modelos preditivos de classificação para sobrevivência

---

## 📁 Estrutura do Projeto
titanic-analysis/
│
├── titanic.ipynb       # Notebook principal com toda a análise
├── LICENSE
└── README.md

---

## 🗂️ Sobre o Dataset

O dataset utilizado é o clássico **Titanic - Machine Learning from Disaster**, disponibilizado pelo [Kaggle](https://www.kaggle.com/competitions/titanic), dividido em dois arquivos:

- `train.csv` — conjunto de treinamento com rótulos de sobrevivência
- `test.csv` — conjunto de teste sem rótulos
- *extra* `titanic.csv` — conjunto completo de dados disponibilizado pelo professor para os exercícios iniciais

| Coluna | Descrição |
|---|---|
| PassengerId | Identificador único do passageiro |
| Survived | Sobreviveu (1) ou não (0) |
| Pclass | Classe no navio (1, 2 ou 3) |
| Name | Nome completo do passageiro |
| Sex | Sexo do passageiro |
| Age | Idade em anos |
| SibSp | Número de irmãos/cônjuges a bordo |
| Parch | Número de pais/filhos a bordo |
| Ticket | Número do bilhete |
| Fare | Preço da passagem |
| Cabin | Número da cabine |
| Embarked | Porto de embarque (C = Cherbourg, Q = Queenstown, S = Southampton) |

---

## 🔍 Etapas da Análise

### 1. Inspeção Inicial
Verificação da estrutura dos dados: dimensões, tipos de variáveis e visualização das primeiras linhas.

### 2. Tipos de Variáveis
Classificação de cada coluna como numérica ou categórica, com identificação do subtipo (discreta/contínua, nominal/ordinal) e das colunas pouco úteis para modelagem.

### 3. Valores Faltantes
Identificação e tratamento de valores ausentes:
- Variáveis numéricas preenchidas com a **mediana por grupo de título** (extraído do nome do passageiro), para uma imputação mais precisa
- Variáveis categóricas preenchidas com a **moda**

### 4. Análise de Outliers
Detecção de outliers nas variáveis `Age` e `Fare` via boxplot e método IQR (1.5 × IQR), com discussão sobre a natureza dos valores discrepantes.

### 5. Distribuições e Histogramas
Visualização das distribuições de `Age` e `Fare`, com análise de assimetria e comparação entre classes de passagem.

### 6. Correlação entre Variáveis
Cálculo e visualização das matrizes de correlação de **Pearson** e **Spearman** entre variáveis numéricas, com identificação de multicolinearidade e das variáveis mais correlacionadas com `Survived`.

### 7. Análise de Grupos
Comparação das taxas de sobrevivência por sexo e classe de passagem, com visualizações e discussão dos possíveis fatores históricos.

### 8. Scatter Plot Bivariado
Gráfico de dispersão entre `Age` e `Fare` com coloração por sobrevivência, explorando padrões visuais entre as variáveis.

### 9. Engenharia de Atributos *(Opcional)*
Criação de novas features como tamanho da família (`FamilySize`) e título extraído do nome, com análise do impacto dessas variáveis na sobrevivência.

---

## 🤖 Modelagem *(Em Desenvolvimento)*

Após a conclusão da EDA, o exercício original disponibilizado pelo professor, serão construídos e avaliados modelos de classificação para prever a sobrevivência dos passageiros, utilizando as bibliotecas **Scikit-learn** e **TensorFlow**.

---

## 🛠️ Tecnologias Utilizadas

- [Python 3](https://www.python.org/)
- [NumPy](https://numpy.org/)
- [Pandas](https://pandas.pydata.org/)
- [Matplotlib](https://matplotlib.org/)
- [Seaborn](https://seaborn.pydata.org/)
- [Scikit-learn](https://scikit-learn.org/)
- [TensorFlow](https://www.tensorflow.org/)

---

## ▶️ Como Executar

1. Clone o repositório:
```bash
git clone https://github.com/seu-usuario/titanic-analysis.git
```

2. Instale as dependências:
```bash
pip install numpy pandas matplotlib seaborn scikit-learn tensorflow
```

3. Abra o notebook:
```bash
jupyter notebook titanic.ipynb
```

Ou importe diretamente no [Google Colab](https://colab.research.google.com/).

---

## 📄 Licença

Este projeto está sob a licença MIT. Consulte o arquivo [LICENSE](./LICENSE) para mais detalhes.
