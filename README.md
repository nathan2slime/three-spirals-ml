
# Classificação das Três Espirais com Redes Neurais

Este projeto aborda o clássico problema de **classificação das três espirais**, uma tarefa não linear e desafiadora para algoritmos de machine learning. Através de uma rede neural profunda construída com TensorFlow/Keras, o modelo aprende a classificar corretamente os pontos pertencentes a três espirais entrelaçadas.

## 🔍 Sobre o Problema

O **problema das três espirais** é um benchmark comum para testar algoritmos de classificação. Consiste em três classes de pontos dispostos em forma de espiral, rotacionadas entre si. A distribuição entrelaçada torna o problema ideal para testar a capacidade de generalização e aprendizagem de modelos complexos.

### Visualização:

Cada espiral representa uma classe:

- 🌀 **Spiral 0**: vermelho  
- 🌀 **Spiral 1**: verde-água  
- 🌀 **Spiral 2**: azul acinzentado

O objetivo é construir um modelo que seja capaz de separar corretamente essas classes mesmo em regiões de sobreposição e ruído.

---

## 🧠 Modelo

Utiliza-se uma **rede neural densa com regularização L2**, camadas de **Batch Normalization**, **Dropout** e função de ativação ReLU. A última camada utiliza `softmax` para classificação multiclasse.

Também foram usados:

- `EarlyStopping` para evitar overfitting
- `ReduceLROnPlateau` para ajuste dinâmico da taxa de aprendizado
- `F1Score` como métrica adicional para avaliar performance por classe

---

## 📦 Instalação

Este projeto utiliza **Poetry** para gerenciamento de dependências. Siga os passos abaixo para configurar o ambiente:

### 1. Clone o repositório:

```bash
git clone https://github.com/seu-usuario/nome-do-repo.git
cd nome-do-repo
```

### 2. Instale o Poetry (se ainda não tiver):

```bash
curl -sSL https://install.python-poetry.org | python3 -
```

> Ou consulte: https://python-poetry.org/docs/

### 3. Instale as dependências do projeto:

```bash
poetry install
```

### 4. Ative o ambiente virtual:

```bash
poetry shell
```

### 5. Execute o script principal:

```bash
jupyter notebook main.ipynb
```

---

## 📊 Resultados

- Acurácia superior a **98%** nos dados de teste.
- **F1-Score** alto para todas as classes, indicando excelente capacidade de generalização.
- Visualizações gráficas como:
  - Evolução do treinamento
  - Matriz de confusão
  - Fronteira de decisão da rede

---

## 📌 Dependências Principais

- `numpy`
- `matplotlib`
- `seaborn`
- `scikit-learn`
- `tensorflow`
- `poetry` (gerenciador)

---

## 📄 Licença

Este projeto está sob a licença MIT. Veja o arquivo `LICENSE` para mais detalhes.

---

## 🤝 Contribuições

Contribuições são bem-vindas! Fique à vontade para abrir uma *issue* ou um *pull request*.