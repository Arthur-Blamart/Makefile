# Makefiles pour C & Java

Ce dépôt fournit des Makefiles génériques pour compiler, exécuter et gérer des projets en C et en Java, avec une séparation claire entre les fichiers sources, les fichiers générés et les exécutables/classes.

## Structure du workspace

```
/
├── c/
│   ├── Makefile
│   └── README.md
├── java/
│   ├── Makefile
│   └── README.md
└── README.md
```

Chaque langage possède son propre dossier avec un Makefile dédié et un README spécifique.

---

## Utilisation générale

- **Initialisation du workspace**  
  Crée les dossiers nécessaires à la compilation :
  ```
  make init
  ```

- **Compilation**  
  Compile tous les fichiers sources :
  ```
  make
  ```

- **Nettoyage**  
  Supprime les fichiers générés :
  ```
  make clean
  ```

---

## Détails par langage

### C

- Les sources `.c` vont dans `c/src/`
- Les headers `.h` vont dans `c/header/`
- Les objets `.o` sont générés dans `c/build/`
- L'exécutable final est placé dans `c/bin/`

**Commandes spécifiques :**
- `make` : compile et lie tous les fichiers pour produire l’exécutable.
- `make clean` : supprime les objets et les exécutables.
- `make cleanBin` : supprime uniquement les exécutables.
- `make cleanBuild` : supprime uniquement les objets.

Voir [c/README.md](c/README.md) pour plus de détails.

---

### Java

- Les sources `.java` vont dans `java/src/`
- Les fichiers `.class` générés sont placés dans `java/classes/`
- Le nom de la classe principale est à adapter dans le Makefile (`MAIN`).

**Commandes spécifiques :**
- `make` : compile tous les fichiers sources.
- `make run` : exécute la classe principale.
- `make clean` : supprime les fichiers `.class`.

Voir [java/README.md](java/README.md) pour plus de détails.

---

## Personnalisation

Les noms des dossiers et des cibles (exécutable ou classe principale) peuvent être modifiés directement dans les Makefiles selon vos besoins.

---

## Ressources

- [c/README.md](c/README.md)
- [java/README.md](java/README.md)

N'hésitez pas à consulter les README de chaque dossier pour des instructions détaillées et des exemples d'utilisation.
