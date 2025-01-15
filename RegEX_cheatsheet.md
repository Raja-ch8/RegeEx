## **1. Classes de caractères**

```
[abc] : Un caractère parmi : a, b ou c.
[^abc] : Un caractère excepté : a, b ou c (le symbole ^ indique la négation dans ce cas).
[a-z] : Un caractère dans l'intervalle : a à z (lettres minuscules).
[^a-z] : Un caractère qui n'est pas dans l'intervalle : a à z (lettres minuscules).
[0-9] : Un chiffre dans l'intervalle : 0 à 9.
[a-zA-Z] : Un caractère dans l'intervalle : a à z ou A à Z (lettres minuscules ou majuscules).
[a-zA-Z0-9] : Un caractère dans l'intervalle : a à z, A à Z ou 0 à 9 (lettres ou chiffres).
```

## **2. Quantificateurs**

```
a? : Zéro ou un caractère de 'a'.
a* : Zéro ou plusieurs caractères de 'a'.
a+ : Un ou plusieurs caractères de 'a'.
[0-9]+ : Un ou plusieurs chiffres de 0 à 9.
a{3} : Exactement 3 caractères de 'a'.
a{3,} : 3 ou plus de caractères 'a'.
a{3,6} : Entre 3 et 6 caractères de 'a'.
a* (quantificateur avide) : Zéro ou plusieurs caractères de 'a' (ce quantificateur est appelé avide car il correspond à autant de caractères 'a' que possible).
a*? (quantificateur paresseux) : Zéro ou plusieurs caractères de 'a' (ce quantificateur est appelé paresseux car il correspond au moins de caractères 'a' possible).
a*+ (quantificateur possessif) : Zéro ou plusieurs caractères de 'a' (ce quantificateur est appelé possessif car il ne revient pas en arrière, il "possède" la correspondance).
```

## **3. Séquences métacaractères**

```
. : N'importe quel caractère.
\s : Tout caractère d'espace blanc (espace, tabulation, retour à la ligne, etc.).
\S : Tout caractère non-espace blanc (tout sauf espace, tabulation, retour à la ligne, etc.).
\d : Tout chiffre, équivalent de [0-9].
\D : Tout caractère non-chiffre, équivalent de [^0-9].
\w : Tout caractère alphanumérique (lettres, chiffres, et underscore _).
\W : Tout caractère non-alphanumérique (tout sauf lettres, chiffres et underscore).
\X : Toute séquence Unicode, y compris les sauts de ligne.
\C : Correspond à une unité de données.
\R : Sauts de ligne Unicode (toutes sortes de sauts de ligne, comme \n, \r\n, etc.).
\v : Caractère d'espace vertical (tabulation verticale, retour chariot vertical).
\V : Négation de \v – tout sauf les sauts de ligne et les tabulations verticales.
\h : Caractère d'espace horizontal (espace, tabulation horizontale).
\H : Négation de \h – tout sauf l'espace horizontal.
\K : Réinitialise la correspondance (utilisé pour "oublier" tout ce qui a été trouvé jusqu'à ce point).
\n : Correspond au n-ième sous-modèle.
\pX : Propriété Unicode X (correspond à une catégorie Unicode spécifique).
\p{...} : Propriété ou catégorie de script Unicode.
\PX : Négation de \pX (tout sauf la propriété Unicode X).
\P{...} : Négation de \p{...}.
\Q...\E : Citer (traite le texte entre \Q et \E comme des littéraux, ce qui signifie que tous les caractères à l'intérieur sont considérés comme des caractères réguliers, non spéciaux).
\k<name> : Correspond à un sous-modèle nommé par son nom (exemple : \k<date>).
\k'name' : Correspond à un sous-modèle nommé par son nom entre guillemets simples.
\k{name} : Correspond à un sous-modèle nommé par son nom entre accolades.
\gn : Correspond au n-ième sous-modèle.
\g{n} : Correspond au n-ième sous-modèle (alternative à \gn).
\g<n> : Recursion du n-ième groupe de capture.
\g'n' : Recursion du n-ième groupe de capture (nommé).
\g{-n} : Correspond au n-ième sous-modèle précédent (relatif).
\g<+n> : Recursion du n-ième sous-modèle suivant (relatif).
\g'+n' : Correspond au n-ième sous-modèle suivant (relatif, avec apostrophes).
\g'letter' : Recursion d'un groupe de capture nommé par sa lettre.
\g{letter} : Correspond au groupe de capture nommé par sa lettre.
\g<letter> : Recursion du groupe de capture nommé par sa lettre.
\xYY : Caractère hexadécimal YY (deux chiffres hexadécimaux).
\x{YYYY} : Caractère hexadécimal YYYY (quatre chiffres hexadécimaux).
\ddd : Caractère octal ddd (trois chiffres octaux).
\cY : Caractère de contrôle Y (comme \cA pour le caractère de contrôle 'A').
[\b] : Caractère de retour arrière (backspace).
\ : Fait tout caractère suivant comme littéral (c'est-à-dire qu'il traite ce caractère comme un caractère normal, sans fonction spéciale).
```


