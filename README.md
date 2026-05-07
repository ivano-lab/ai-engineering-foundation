# AI Engineering Foundation: From Scratch to Production

> **"Software engineering is the art of managing complexity. AI engineering is the art of managing complexity when the logic is probabilistic."**

Este repositório é o meu laboratório pessoal e público de fundamentos em Engenharia de IA. O objetivo aqui é triplo:
1. **Combater a Atrofia Cognitiva:** Implementar algoritmos do zero (From Scratch) para entender a matemática e a física por trás dos modelos.
2. **Eliminar Débito Técnico:** Masterizar a transição entre abstrações de alto nível (Python/PyTorch) e controle de baixo nível (C++/Hardware).
3. **Reprodutibilidade:** Servir como um guia pedagógico para estudantes e recrutadores sobre como construir uma base sólida em IA.

---

## Estrutura

O aprendizado é dividido em módulos que evoluem em complexidade e proximidade com o hardware.

### 01. Mathematical Foundations (`/01-math`)
Implementações puras em **NumPy** e **C++** focado em:
* **Álgebra Linear:** Multiplicação de tensores, decomposição de matrizes.
* **Cálculo:** Implementação manual de Backpropagation e otimizadores (SGD, Adam).
* **Probabilidade:** Entropia e Divergência KL.

### 02. The Core: Mechanisms (`/02-mechanisms`)
Onde a "mágica" acontece. Foco inicial na arquitetura **Transformer**:
* **Scaled Dot-Product Attention:** Implementação passo a passo e documentação do impacto do fator de escala $\sqrt{d_k}$.
* **Multi-Head Attention:** Paralelização da atenção.
* **Positional Encoding:** Por que o modelo precisa de noção de ordem?

### 03. The Metal: Performance & C++ (`/03-cpp-inference`)
Enfrentando o meu maior desafio: **C++**.
* Gestão manual de memória para Tensores.
* Implementação de funções de ativação (ReLU, Softmax) em C++.
* Benchmarking: Python vs C++ em operações de matriz.

### 04. Deep Learning Systems (`/04-systems`)
Engenharia de software aplicada à IA:
* Design de Microserviços para modelos (inferência assíncrona).
* Estratégias de Quantização (FP16, INT8).
* Integração com Docker e Kubernetes para escalonamento.

---

## Stack Tecnológica
* **Linguagens:** Python (Orquestração), C++ (Performance), JavaScript (Visualização/Web).
* **Frameworks:** PyTorch, NumPy, Docker.
* **Ambiente:** GitHub Codespaces & Linux (Ubuntu/Arch).

---

## Eureka Moments

*   Implementação do Scaled Dot-Product Attention. C++ obriga a entender o *Memory Layout* (Row-major) de uma forma que o NumPy esconde. A abstração só é segura quando você conhece o que ela está ocultando.

---

## Como utilizar este repo
Cada subpasta contém um arquivo `EXPLICAÇÃO.md` que detalha a matemática por trás do código e as escolhas de engenharia feitas.
