# Projeto Final - Inteligência Artificial

## Sistema Inteligente de Triagem Hospitalar com Rede Bayesiana e Busca A*

## Descrição

Este projeto foi desenvolvido para a disciplina de Inteligência Artificial e implementa um sistema de triagem hospitalar inteligente.

O sistema utiliza uma Rede Bayesiana para estimar a probabilidade de um paciente apresentar um quadro de alta gravidade a partir de seus sinais vitais. Com base nessa estimativa, são comparadas diferentes estratégias de atendimento para identificar aquela que minimiza o risco acumulado durante a fila de espera.

Todo o desenvolvimento foi realizado em um Jupyter Notebook (`.ipynb`), contendo explicações, implementação e testes.

---

## Objetivos

- Modelar uma Rede Bayesiana para inferência de gravidade.
- Calcular a probabilidade de gravidade de cada paciente.
- Comparar diferentes estratégias de atendimento.
- Avaliar o risco acumulado de cada estratégia.

---

## Técnicas de Inteligência Artificial

### Rede Bayesiana

A Rede Bayesiana estima a probabilidade de um paciente estar em estado grave utilizando as seguintes evidências:

- Temperatura corporal (Febre);
- Saturação de oxigênio;
- Pressão arterial.

O resultado da inferência é a probabilidade:

```text
P(Gravidade = Alta)
```

Essa probabilidade é utilizada no cálculo do risco de cada paciente.

### Algoritmos de Busca

Foram implementadas três estratégias de atendimento:

- **FIFO (First In, First Out):** atende os pacientes na ordem de chegada.
- **Busca Gulosa:** seleciona o paciente com maior risco imediato.
- **Busca A\*:** utiliza uma função heurística para encontrar a ordem de atendimento que minimize o risco acumulado.

---

## Cálculo do Risco

O risco de cada paciente é calculado considerando:

- A probabilidade de gravidade estimada pela Rede Bayesiana;
- O tempo de espera do paciente.

Ao final do atendimento é calculado o **Risco Acumulado Total**, utilizado para comparar o desempenho das diferentes estratégias.

---

## Estrutura do Projeto

```text
Projeto-Final-IA/

├── Projeto_Final_IA.ipynb
├── README.md
└── requirements.txt (opcional)
```

---

## Como Executar

### 1. Clone o repositório

```bash
git clone <url-do-repositorio>
```

### 2. Acesse a pasta do projeto

```bash
cd Projeto-Final-IA
```

### 3. Instale as dependências

```bash
pip install pgmpy numpy pandas networkx matplotlib
```

### 4. Abra o notebook

```bash
jupyter notebook
```

ou

```bash
jupyter lab
```

Em seguida, abra o arquivo `Projeto_Final_IA.ipynb` e execute todas as células na ordem em que estão organizadas.

---

## Bibliotecas Utilizadas

- Python 3
- Jupyter Notebook
- pgmpy
- NumPy
- Pandas
- NetworkX
- Matplotlib

---

## Organização do Notebook

O notebook está dividido nas seguintes etapas:

1. Importação das bibliotecas;
2. Construção da Rede Bayesiana;
3. Definição das probabilidades condicionais;
4. Testes da Rede Bayesiana;
5. Definição dos pacientes;
6. Cálculo do risco individual;
7. Implementação das estratégias FIFO, Busca Gulosa e Busca A*;
8. Comparação dos resultados obtidos.

---

## Autores

Projeto desenvolvido para a disciplina de Inteligência Artificial.

**Integrantes do grupo:**

- Bruno Henrique Pacheco Prudêncio
- Matheus Alves Cavalcante

---
