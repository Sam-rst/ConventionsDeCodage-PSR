# Conventions de Codage

Ce document va vous permettre de connaître les bonnes conventions de codage lors de projets en collaborations.

## Nomenclature
Nommer ses variables correctement selon des conventions officielles.
```python
# Variables (camelCase ou snake_case)
maVariable = 0

# Classes (PascalCase)
class MaClasse:

# Constantes (SCREAMING_SNAKE_CASE)
PI = 3.1415
```

## Indentation
Utilisez des espaces pour l'indentation, pas de tabulations.
```python
# Mauvais
def fonction():
    \tinstruction()

# Bon
def fonction():
    instruction()
```

## Commentaires :
Écrire des commentaires clairs et concis pour expliquer le code complexe ou les parties importantes
```python
# Mauvais
x = x + 1  # Ajouter 1 à x

# Bon
x = x + 1  # Incrémente x de 1
```

## Longueur des lignes :
Les lignes de code ne doivent pas dépasser 80 caractères.
```python
# Mauvais
resultat = fonction_tres_longue(arg1, arg2, arg3, arg4, arg5, arg6)

# Bon
resultat = fonction_tres_longue(
    arg1, arg2, arg3, arg4, arg5, arg6
)
```

## Importations :
Regrouper les importations par type (modules standard, bibliothèques tierces, modules locaux) et séparer chaque groupe par une ligne vide.
```python
# Mauvais
import os, sys
from module1 import fonction1, classe1
from module2 import fonction2

# Bon
import os
import sys

from module1 import fonction1, classe1
from module2 import fonction2
```

## Documentation :
Inclure des docstrings pour chaque fonction, méthode, classe et module pour expliquer leur fonctionnement et leurs paramètres.
```python
# Mauvais
def calculer(x, y):
    """Fonction pour calculer."""
    return x + y

# Bon
def calculer(x, y):
    """Calcule la somme de deux nombres.

    Args:
        x (int): Premier nombre.
        y (int): Deuxième nombre.

    Returns:
        int: Somme de x et y.
    """
    return x + y
```

## Factorisation de Code
Éviter la duplication de code en factorisant les fonctionnalités répétitives dans des fonctions ou des méthodes.
```python
# Mauvais
resultat1 = x * 2
resultat2 = x * 2

# Bon
def doubler(nombre):
    return nombre * 2

resultat1 = doubler(x)
resultat2 = doubler(x)
```
