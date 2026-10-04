# Nebula Hub — builds macOS

Builds macOS de [Nebula-Hub](https://github.com/Memel-SQT/Nebula-Hub), téléchargeables dans les [Releases](../../releases).

- Le code de l'app vient tel quel du dépôt d'origine, à chaque nouveau commit sur `main`.
- Seuls les patchs de [`patches/`](patches) sont ajoutés. Ils ne concernent **que macOS** (chaque modification est gardée par `process.platform === 'darwin'`, une option propre à la plateforme Mac, ou une branche équivalente) : les builds Windows et Linux du dépôt d'origine ne changent pas.
- Les bugs macOS sont décrits dans [`bug-reports/macos/`](https://github.com/Memel-SQT/Nebula-Hub/tree/main/bug-reports/macos) du dépôt d'origine.

## Installation (app non signée)

Ces builds ne sont ni signés ni notarisés par Apple. Au premier lancement, macOS peut dire que l'app « est endommagée » ou « ne peut pas être ouverte ». Après l'avoir copiée dans Applications :

```bash
xattr -cr "/Applications/Nebula Hub.app"
```

ou bien clic droit → Ouvrir. Fichiers : `-arm64` pour les Mac Apple Silicon (M1 et suivants), `-x64` pour les Mac Intel.

La mise à jour automatique intégrée ne fonctionne pas sur macOS pour une app non signée : installez simplement la release Mac suivante.

## Limites connues sur macOS
- Le Hub est conçu pour Windows : sur macOS il **ne détecte pas, n'installe pas et ne lance pas** les autres apps Nebula (registre Windows, `tasklist.exe`, installeurs `.exe`). L'interface, le catalogue et les réglages fonctionnent.
- Nebula Link (named pipe Windows) n'est pas fiable sur macOS.
