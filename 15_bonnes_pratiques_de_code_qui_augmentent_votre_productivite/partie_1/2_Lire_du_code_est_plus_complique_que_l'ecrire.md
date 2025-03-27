
# 2. Lire du code est plus compliqué que l'écrire

```python
def f(i,j):print(i);f(j,i+j)
```

```python
def fibonacci(n: int) -> int:
    if n < 0:
        print("Input incorrect")
    if n == 0:
        return 0
    if n == 1 or n == 2:
        return 1

	return fibonacci(n-1) + fibonacci(n-2)
```

```haskell
f=1:scanl(+)1f
```

```perl
^2,*+*...*
```

```python
def calcul_fibonacci(n_entier_positif: int) -> int:
    resultat_final = None
    valeur_de_retour_pour_zero = 0
    valeur_de_retour_pour_un_ou_deux = 1
    texte_erreur_input_incorrect = "Input incorrect"

    condition_si_entree_est_negative = n_entier_positif < 0
    condition_si_entree_egale_zero = n_entier_positif == 0
    condition_si_entree_est_un_ou_deux = n_entier_positif == 1 or n_entier_positif == 2

    if condition_si_entree_est_negative:
        raise EntreeNegativePourFibonacciQuiAttendsDuPositifException()

    if condition_si_entree_egale_zero:
        resultat_final = valeur_de_retour_pour_zero
        return resultat_final
    
    # Vérification si l'entrée est égale à un ou deux
    if condition_si_entree_est_un_ou_deux:
        resultat_final = valeur_de_retour_pour_un_ou_deux
        return resultat_final
    
    # Calcul récursif de Fibonacci
    valeur_a_soustraire_pour_le_premier_appel_recursif = 1
    valeur_a_soustraire_pour_le_second_appel_recursif = 2
    premier_argument_recursif = n_entier_positif - valeur_a_soustraire_pour_le_premier_appel_recursif
    deuxieme_argument_recursif = n_entier_positif - valeur_a_soustraire_pour_le_second_appel_recursif
    
    resultat_final = calcul_fibonacci(premier_argument_recursif) + calcul_fibonacci(deuxieme_argument_recursif)
    
    return resultat_final
```
