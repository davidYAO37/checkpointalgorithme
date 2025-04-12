
# Algorithmes - Tableaux et Vecteurs

## Problème 1 : Somme des éléments distincts de deux tableaux

### Description
On a deux tableaux A et B. On veut faire la somme des éléments qui ne sont présents **que dans un seul** des deux tableaux.

### Algorithme simple
```plaintext
Variables :
  A, B : tableaux d'entiers
  nA, nB : entiers
  i, j : entiers
  est_dans_B, est_dans_A : booléens
  somme : entier

Début
  somme ← 0

  Pour i de 1 à nA faire
    est_dans_B ← faux
    Pour j de 1 à nB faire
      Si A[i] = B[j] alors
        est_dans_B ← vrai
      FinSi
    FinPour
    Si est_dans_B = faux alors
      somme ← somme + A[i]
    FinSi
  FinPour

  Pour j de 1 à nB faire
    est_dans_A ← faux
    Pour i de 1 à nA faire
      Si B[j] = A[i] alors
        est_dans_A ← vrai
      FinSi
    FinPour
    Si est_dans_A = faux alors
      somme ← somme + B[j]
    FinSi
  FinPour

  Afficher "Somme des éléments distincts : ", somme
Fin
```

---

## Problème 2 : Produit scalaire et orthogonalité

### Partie 1 : Procédure `dot_product`
```plaintext
Procédure dot_product(V1, V2, N, ps)
Variables :
  i : entier
Début
  ps ← 0
  Pour i de 1 à N faire
    ps ← ps + V1[i] * V2[i]
  FinPour
FinProcédure
```

### Partie 2 : Vérifier l'orthogonalité
```plaintext
Variables :
  V1, V2 : tableaux d'entiers
  N, ps : entier

Début
  Appeler dot_product(V1, V2, N, ps)

  Si ps = 0 alors
    Afficher "Les vecteurs sont orthogonaux"
  Sinon
    Afficher "Les vecteurs ne sont pas orthogonaux"
  FinSi
Fin
```

---

> Ces algorithmes utilisent un style simple et clair, adaptés à un contexte scolaire ou de début de formation algorithmique.
