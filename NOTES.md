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
