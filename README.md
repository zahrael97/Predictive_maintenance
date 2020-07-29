# Maintenance prédictive : Prédire la panne de la pompe à eau
utilisation des techniques d’apprentissage automatique pour prédire la panne de la pompe à eau avant qu’elle ne se produise.

# Problème
une équipe qui qui prend en charge les pompes à eau d’une petite zone, a eu 7 pannes de systéme l’année derniére.
Ces ́echecs causent un ́enorme probléme pour de nombreuses personnes et en-traînent également de graves problémes de vie pour certaines familles. L’ ́equipe ne voit aucun motif dans le données lorsque le systéme tombe en panne, de sorte qu’ils ne savent pas où mettre plus d’attention.


![Image of Yaktocat](https://github.com/zahrael97/Predictive_maintenance/blob/master/img/pump.jpg)
# Dataset

L'ensemble de données est extrait de Kaggle et contient des informations provenant de 52 capteurs différents.
Le résultat contient trois catégories: NORMAL, RECOVERY, BROKEN.

# Approches
Deux approches: apprentissage automatique et LSTM . 

# Modèle
LSTM est un réseau neuronal complexe avec une cellule de mémoire, une entrée, une sortie et
oublier (portes) (voir la figure ci-dessous). La cellule de mémoire peut stocker les données précédentes dans une quantité spécifiée, ce qui
peut être utilisé pour aider à améliorer la prédiction. À l'aide d'un portail, il est possible d'ajouter ou de supprimer
informations dans une cellule.

# la mise en oeuvre
Le LSTM multicouche (2-LSTM) est formé. La première couche est une couche LSTM avec 100 unités suivie d'une autre couche LSTM avec 50 unités. La suppression est également appliquée après chaque couche LSTM pour contrôler le surajustement. La couche finale est une couche de sortie dense avec une unité et une activation sigmoïde car il s'agit d'un problème de classification binaire. le réseau est optimisé avec Adam.
