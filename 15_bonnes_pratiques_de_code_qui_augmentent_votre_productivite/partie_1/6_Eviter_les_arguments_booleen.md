# 6. Eviter les arguments booléen

```python
def est_nombre_valide(s: str, accepte_negatif: bool) -> bool:
	try:
		number = int(s)
	except ValueError:
		return False

	if accepte_negatif:
		return True

	if number < 0:
		return False

	return True


def est_nombre_valide(s: str) -> bool:
	try:
		int(s)
	except ValueError:
		return False
	return True

def est_nombre_valide_positif(s: str) -> bool:
	if estNombreValide(s) and not '-' in s:
		return True
	return False
```

```python
class Maison:
	def __init__(self, chambres: int, piscine: bool, jardin: bool, garage: bool):
		pass

# Bon courage pour retenir l'ordre des booléens, ou comprendre cette ligne rapidement.
maison = Maison(3, false, true, false, false)

class MaisonBuilder:
	def __init__(self):
		self.chambres = 0
		self.piscine = False
		self.jardin = False
		self.garage = False

	def a_chambre(self, n):
		self.chambres = n

	def a_piscine(self):
		self.piscine = True

	def a_jardin(self):
		self.jardin = True

	def a_garage(self):
		self.garage = True

	def build(self) -> Maison:
		return Maison(self.chambres, self.piscine, self.jardin, self.garage)

maison_builder = MaisonBuilder()
maison_builder.a_chambre(3)
maison_builder.a_jardin()
maison = maison_builder.build()


# Ou encore, en modifiant légèrement les fonctions précédentes 

def a_chambre(self, n):
    self.chambres = n
    return self  # Pour chaîner les méthodes, comme ci dessous:

maison = MaisonBuilder() \
	.a_chambre(3) \
	.a_jardin() \
	.build()
```