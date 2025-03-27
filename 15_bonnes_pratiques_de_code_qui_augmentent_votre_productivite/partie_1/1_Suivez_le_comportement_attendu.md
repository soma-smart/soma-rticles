# 1. Suivez le comportement attendu

```python
def add(a: int, b: int) -> int:
	return a * b  # Add fait une muliplication ?


def est_valid(b: bool) -> bool:
	if b:
		return True
	else:
		# Un retour booléen qui renvoie une Exception
		# à la place de False ?
		raise ValueError()


@router.get("{item}")
def get_item(item: str):
	# Une requête HTTP GET est supposée être une requête de lecture
	# Pas une requête de modification
	items.append(item)
```