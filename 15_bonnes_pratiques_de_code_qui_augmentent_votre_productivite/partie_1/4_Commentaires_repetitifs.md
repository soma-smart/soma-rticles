# 4. Commentaires répétitifs

```python
# Liste d'items
items = []

# Ajoute les chiffres de 0 à 9 à la liste
for i in range(10): 
	items.append(i)

def concat(s1: str, s2: str) -> str:
	"""Concatène des strings
	Arguments:
		s1 (str): première string
		s2 (str): seconde string

	Retourne:
		string: strings concaténés
	"""
	return s1 + s2
```

```python
# Calcule l'aire d'un rectangle
def mult(a: int, b: int) -> int:
	"""
	Arguments:
		a (int): côté long du rectangle
		b (int): côté large du rectangle

	Retourne:
		int: Aire du rectangle
	"""
	return a * b



def calcule_aire_rectangle(largeur: int, longueur: int) -> int:
	return largeur * longueur
```

```python
from typing import Generator
def exemple_generator(n) -> Generator[int, None, None]:
    """Retourne un generator plus optimisé pour les grands nombres.

    Args:
        n (int): Limite haute du générateur. De 0 à n - 1

    Yields:
        int: L'entier suivant de 0 à n - 1

    Exemples:
        >>> print([i for i in exemple_generator(4)])
        [0, 1, 2, 3]

		>>> print([i**2 for i in exemple_generator(6)])
		[0, 1, 4, 9, 16, 25]

    """
    for i in range(n):
        yield i
```