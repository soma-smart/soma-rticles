# 5. Encapsule les conditions

```python
if (annee % 4 == 0 and (annee % 100 != 0 and annee % 400)):
	jours = 366


# En divisant les règles, on comprends ce qui a voulu être fait plus facilement
def est_bissextile(annee) -> bool:
	est_divisible_par_4 = (annee % 4 == 0)
	est_pas_divisible_par_100 = (annee % 100 != 0)
	est_divisible_par_400 = (annee % 400 == 0)

	return (
		est_divisible_par_4 and (
			est_pas_divisible_par_100 or
			est_divisible_par_400
		)
	)

if (est_bissextile(annee)):
	jours = 366
```