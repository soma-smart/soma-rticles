# 3. Noms de variables explicites

```python
# l pour les listes
l = []

# i, j, k pour les iterations
for i in range(10):
    for j in range(10):
        for k in range(10):
            print(i, j, k)

# a et b pour deux éléments
def sum(a: int, b: int):
    return a + b

# Ou encore left et right
def sum(left: int, right: int):
    return left + right

# f pour les fichiers
with open('file.csv', 'r') as f: 
    f.read()
```

```python
for longueur in range(10):
    for largeur in range(10):
        for hauteur in range(10):
            print(longueur, largeur, hauteur)


# Donc aucune voiture
voitures_louees = []
```