## Algorithme : AnalyserPhrase (en langage algorithmique simple)

```algo
Variables :
    caractere : caractère
    longueur, mots, voyelles : entier
    precedent : caractère
    phrase : chaîne

Début
    longueur ← 0
    mots ← 0
    voyelles ← 0
    precedent ← ' '

    Ecrire "Entrez une phrase qui se termine par un point :"
    Lire phrase

    Pour i de 1 à Longueur(phrase) faire
        caractere ← Caractere_i(phrase, i)  // récupère le i-ème caractère

        longueur ← longueur + 1

        // Vérifie si un mot commence
        Si caractere ≠ ' ' et (precedent = ' ' ou i = 1) alors
            mots ← mots + 1
        Fin Si

        // Vérifie si c’est une voyelle
        Si Minuscule(caractere) = 'a' ou Minuscule(caractere) = 'e' ou
           Minuscule(caractere) = 'i' ou Minuscule(caractere) = 'o' ou
           Minuscule(caractere) = 'u' ou Minuscule(caractere) = 'y' alors
            voyelles ← voyelles + 1
        Fin Si

        precedent ← caractere
    Fin Pour

    Ecrire "Longueur de la phrase : ", longueur
    Ecrire "Nombre de mots : ", mots
    Ecrire "Nombre de voyelles : ", voyelles
Fin
```

### Remarques :

- `Caractere_i(phrase, i)` : fonction imaginaire pour prendre le iᵉ caractère.
- `Minuscule(caractere)` : convertit une lettre en minuscule.
- La phrase doit se terminer par un **point (.)** comme exigé.
