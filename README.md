# GRE-Labo3-Assemblee

## Modélisation du problème

On peut modéliser ce problème par un problème de transbordement. 
Pour cela on utilise le graphe suivant :
- Des sommets $D_j, ~ j \in [ 1,10 ]$ représentant les districts, avec une offre de $l_j$ pour garantir ce minimum,

- Un sommet source $S$, avec une offre de $\displaystyle p - \sum_{j=0}^{10}l_j$ pour représeter l'offre non donnée par les districts,

- Des arcs $S \rightarrow D_j ~(\forall j \in [1,10])$ de capacité $u_j - l_j$ pour permettre d'aller jusqu'au maximum mais pas au delà,

- Des sommets $C_i, ~ i \in [1,n]$ représentant les candidats,

- Des sommets $S_k, ~ k \in [1,p]$ représentant les sociétés de 
gymnastique, de demande 1 pour que chaque société aie un délégué,

- Des arcs $D_j \rightarrow C_i$ lorsque le candidat $i$ habite dans le district $j$, de capacité 1 pour s'assurer que le candidat sera choisi pour une seule place de délégué (dans le cas où il est membre de plusieurs sociétés),

- Des arcs $C_i \rightarrow S_k$ lorsque le candidat $i$ fait partie de la société $k$, sans capacité (ou une capacité de 1).