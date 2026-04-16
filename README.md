# T4 – Problema do Caixeiro Viajante

Implementação das heurísticas **Nearest Insertion** e **Smallest Insertion** para o TSP em **Python**, baseada na estrutura fornecida em `Tour.java` / `Main.java`.

---

## Heurísticas implementadas

### `insertNearest(p)`
Encontra a cidade **mais próxima de `p`** já presente no circuito e insere `p` imediatamente após ela.

### `insertSmallest(p)`
Para cada aresta `(a → b)` do circuito atual, calcula o custo de inserção:

```
custo = dist(a, p) + dist(p, b) − dist(a, b)
```

Insere `p` na posição de **menor custo incremental**.

---

## Estrutura

```
t4-tsp/
├── README.md
├── dados/
│   ├── tsp10.txt
│   ├── tsp10-nearest.txt
│   ├── tsp10-smallest.txt
│   ├── tsp10-optimal.txt
│   └── usa13509.txt
└── src/
    ├── main.py
    ├── point.py
    ├── tour.py
    └── visualizer.py
```

---

## Dependências

```bash
pip install matplotlib
```

---

## Execução

```bash
cd src

# Instância de depuração (10 cidades)
python main.py ../dados/tsp10.txt

# Instância principal (13 509 cidades)
python main.py ../dados/usa13509.txt
```

---

## Link do vídeo

> [*(Clique aqui)*](https://youtu.be/MccEkkiFdUA)
