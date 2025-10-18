# TP_GESE_S1

TP pour GESE 1 FST SETTAT

## Installation et configuration pour le développement en C (Windows)

Ce guide explique comment installer Visual Studio Code, un compilateur C (MinGW-w64 via MSYS2), l'extension C/C++ pour VS Code, et comment compiler/exécuter un programme "Hello World" en C depuis PowerShell.

### 1) Installer Visual Studio Code

- Télécharge et installe Visual Studio Code (stable) :

  https://code.visualstudio.com/

- Pendant l'installation, tu peux cocher les options utiles :
  - "Add to PATH" (pratique pour lancer `code` depuis un terminal)
  - "Register Code as an editor for supported file types"

### 2) Installer un compilateur C sur Windows (MSYS2 + mingw-w64)

La méthode recommandée est d'utiliser MSYS2, qui fournit des paquets récents et faciles à maintenir pour mingw-w64.

1. Télécharge MSYS2 et suis l'installateur : https://www.msys2.org/
2. Lance l'environnement MSYS2 (choisis "MSYS2 MSYS" pour les mises à jour puis "MSYS2 MinGW 64-bit" pour travailler en 64-bit).
3. Mets à jour la base de paquets (dans la fenêtre MSYS2) :

```powershell
pacman -Syu
# Si le terminal se ferme après cette commande, relance MSYS2 puis exécute :
pacman -Su
```

4. Installe la toolchain MinGW-w64 (64-bit) :

```powershell
pacman -S --needed base-devel mingw-w64-x86_64-toolchain
```

5. Ouvre "MSYS2 MinGW 64-bit" pour utiliser `gcc` et `g++` (les binaires seront disponibles dans cet environnement).

Remarques :
- Si tu préfères une alternative plus simple, tu peux installer MinGW-w64 standalone ou TDM-GCC, mais MSYS2 est recommandé pour sa maintenance et ses paquets à jour.
- Pour que `gcc` soit accessible depuis PowerShell / le terminal de VS Code, ajoute le chemin MinGW (par ex. `C:\msys64\mingw64\bin`) à la variable d'environnement PATH, ou utilise le terminal intégré MinGW dans VS Code.

### 3) Installer l'extension C/C++ dans VS Code

1. Ouvre Visual Studio Code.
2. Va dans l'onglet Extensions (ou appuie sur Ctrl+Shift+X).
3. Recherche et installe "C/C++" par Microsoft (identifiant : ms-vscode.cpptools).
4. Optionnel : installe "C/C++ Extension Pack" ou "Code Runner" pour des fonctionnalités additionnelles.

### 4) Exemple : Hello World en C

1. Crée un fichier `hello.c` dans le dossier du projet avec ce contenu :

```c
#include <stdio.h>

int main(void) {
    printf("Hello, world!\n");
    return 0;
}
```

2. Compiler et exécuter depuis PowerShell (si `gcc` est dans le PATH) :

```powershell
# Compiler
gcc -o hello.exe hello.c

# Exécuter
.\hello.exe
```

Si tu utilises MSYS2, ouvre le terminal "MSYS2 MinGW 64-bit" dans VS Code pour que `gcc` soit disponible.

### 5) Suggestions de configuration dans VS Code

- Terminal intégré : ouvre le terminal intégré (Ctrl+`) et choisis le shell MinGW pour compiler directement dans VS Code.
- Tâche de build (optionnel) : tu peux ajouter une tâche dans `.vscode/tasks.json` pour automatiser la compilation. Exemple minimal :

```json
{
  "version": "2.0.0",
  "tasks": [
    {
      "label": "build hello",
      "type": "shell",
      "command": "gcc -o hello.exe hello.c",
      "group": "build",
      "problemMatcher": []
    }
  ]
}
```

### 6) Remarques finales

- Sous Windows, les exécutables sont des fichiers `.exe` et s'exécutent par `.\nom.exe` dans PowerShell.
- Si tu rencontres des problèmes (gcc non trouvé, erreurs de compile), vérifie que le binaire `gcc` est dans le PATH ou que tu utilises le terminal MinGW fourni par MSYS2.

Bon développement !
