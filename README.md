
# 🎨 Algoritmos de Coloração de Grafos

Este projeto implementa e compara diferentes algoritmos de coloração de grafos em Python, utilizando a biblioteca `networkx`. A coloração de grafos é uma técnica importante na Teoria dos Grafos, onde o objetivo é atribuir cores aos vértices de um grafo de forma que vértices adjacentes não compartilhem a mesma cor.

## 📌 Funcionalidades

- Implementação de três algoritmos de coloração:
  - 🎯 **Coloração Exata** (backtracking com k cores)
  - ⚡ **Coloração Gulosa**
  - 📊 **Coloração Gulosa Ordenada por Grau**
- Geração de grafos aleatórios usando o modelo Erdős–Rényi.
- Verificação de validade da coloração.
- Visualização gráfica do grafo com as cores atribuídas.
- Benchmarking com tempo de execução e número de cores utilizadas.

## 🧪 Algoritmos Implementados

### 1. `colorir_com_k_cores(grafo, k)`
Coloração exata via backtracking. Tenta colorir o grafo com no máximo `k` cores, garantindo que nenhum vértice adjacente compartilhe a mesma cor.

### 2. `colorir_guloso(grafo)`
Coloração gulosa simples: percorre os vértices em ordem e atribui a menor cor disponível que não esteja sendo usada pelos vizinhos.

### 3. `colorir_guloso_ordenado(grafo)`
Versão aprimorada do guloso: ordena os vértices por grau (do maior para o menor) antes de aplicar a coloração.

## 📊 Exemplo de Saída

```
🧪 Teste 1
Nós: 8 | Arestas: 14
----------------------------------------
🎯 Exato      | Cores: 4 | Válido: True | Tempo: 0.0021s
⚡ Guloso     | Cores: 5 | Válido: True | Tempo: 0.0002s
📊 Ordenado   | Cores: 4 | Válido: True | Tempo: 0.0003s
```

> O script exibe o número de cores utilizadas, se a coloração é válida, e o tempo de execução para cada algoritmo.

## 🖼 Visualização

A visualização dos grafos coloridos é feita com `matplotlib`. O primeiro teste exibe três grafos com coloração aplicada:

- 🎯 Coloração Exata
- ⚡ Coloração Gulosa
- 📊 Coloração Ordenada

## 🚀 Como Executar

1. Certifique-se de ter o Python 3 instalado.
2. Instale as dependências:

```bash
pip install networkx matplotlib
```

3. Execute o script:

```bash
python nome_do_arquivo.py
```

> Altere `nome_do_arquivo.py` para o nome real do seu script.

## 🔧 Parâmetros Personalizáveis

Na função `testar_algoritmos()` você pode configurar:

- `num_testes`: número de testes a serem realizados.
- `num_vertices`: número de vértices dos grafos aleatórios.
- `prob_arestas`: probabilidade de criação de arestas entre os vértices.

```python
testar_algoritmos(num_testes=5, num_vertices=8, prob_arestas=0.5)
```

## 📚 Bibliotecas Utilizadas

- [`networkx`](https://networkx.org/) – criação e manipulação de grafos.
- [`matplotlib`](https://matplotlib.org/) – visualização dos grafos.
- `random`, `time` – geração de dados e medição de desempenho.

## 📄 Licença

Este projeto está sob a licença MIT. Sinta-se livre para usar, modificar e compartilhar.
