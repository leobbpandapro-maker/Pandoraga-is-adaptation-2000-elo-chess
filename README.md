# 馃惣 Pandoraga Full Adaptation 惟

Moteur d'茅checs Python orient茅 recherche, adaptation statistique locale et interface graphique Tkinter.

> **脡tat du d茅p么t :** paquet de publication pr茅par茅 脿 partir du fichier Pandoraga 惟 fourni dans les fichiers du projet. La compilation syntaxique Python a 茅t茅 v茅rifi茅e. Le fonctionnement complet de l'interface, toutes les r猫gles d'茅checs et la force Elo n'ont pas 茅t茅 valid茅s ind茅pendamment : faites les tests d茅crits ci-dessous avant de pr茅senter une version comme stable.

## Fonctionnalit茅s annonc茅es par le projet

- Recherche d'茅checs avec Negamax / Alpha-Beta et am茅liorations de recherche pr茅sentes dans le code.
- Profondeur et temps de r茅flexion adaptatifs, dans les limites d茅finies par le moteur.
- M茅moire locale JSON pour les donn茅es d'adaptation.
- Interface graphique Tkinter.
- Mode Stockfish optionnel, si la version du programme et le syst猫me utilis茅 le prennent en charge et si Stockfish est install茅 s茅par茅ment.
- Fonctionnement local ; aucune connexion r茅seau n'est n茅cessaire au moteur de base.

Les 茅l茅ments ci-dessus d茅crivent les objectifs et 茅l茅ments pr茅sents dans le code, pas une certification ind茅pendante de leur exactitude ni une garantie de niveau Elo.

## Pr茅requis

- Python 3.10 ou plus r茅cent recommand茅.
- Tkinter disponible dans l'installation Python pour utiliser la fen锚tre graphique.
- Aucun paquet `pip` n'est requis par le fichier principal.
- Stockfish est facultatif et n'est pas distribu茅 dans ce d茅p么t.

## D茅marrage

### Windows

1. Installez Python depuis le site officiel et activez l'option d'ajout au `PATH`.
2. Ouvrez un terminal dans le dossier du projet.
3. Lancez :

```powershell
py Pandoraga.py
```

Vous pouvez aussi lancer `run_windows.bat`.

### Linux

V茅rifiez que Python et Tkinter sont install茅s, puis ex茅cutez :

```bash
python3 Pandoraga.py
```

### Android

Le code utilise Tkinter : beaucoup d'environnements Python Android ne le prennent pas en charge. Le fichier n'est donc **pas garanti compatible Android** sans environnement graphique compatible.

## M茅moire et confidentialit茅

Le moteur utilise un fichier de m茅moire JSON local nomm茅 `pandoraga_memoire.json` (ou le nom d茅fini dans le code). Ce fichier peut contenir des donn茅es de parties ou d'adaptation. Ne publiez pas votre m茅moire personnelle dans GitHub ; elle est exclue par `.gitignore`.

## V茅rification rapide

```bash
python -m py_compile Pandoraga.py
```

Cette commande v茅rifie la syntaxe, pas la qualit茅 des coups ni le fonctionnement de la GUI. Avant une publication stable, v茅rifiez notamment : coups l茅gaux, roque, en passant, promotions, 茅chec et mat, pat, r茅p茅tition, arr锚t de recherche, sauvegarde/chargement JSON et fermeture propre de l'application.

## Limites importantes

- La profondeur maximale configur茅e n'est pas une promesse que chaque coup atteindra cette profondeur : le temps, le mat茅riel et la complexit茅 de la position comptent.
- Le score d'茅valuation n'est pas un classement Elo officiel.
- L'adaptation JSON/statistique ne doit pas 锚tre d茅crite comme un r茅seau neuronal entra卯n茅 si aucun tel mod猫le n'est pr茅sent.
- Ne pr茅sentez pas 芦 2000 Elo 禄 ou un autre niveau comme acquis sans un protocole de parties mesur茅 et reproductible.

## Structure

```text
Pandoraga-Full-Adaptation-Omega/
鈹溾攢鈹€ Pandoraga.py
鈹溾攢鈹€ README.md
鈹溾攢鈹€ LICENSE
鈹溾攢鈹€ CHANGELOG.md
鈹溾攢鈹€ CONTRIBUTING.md
鈹溾攢鈹€ SECURITY.md
鈹溾攢鈹€ .gitignore
鈹溾攢鈹€ run_windows.bat
鈹溾攢鈹€ docs/
鈹�   鈹溾攢鈹€ ARCHITECTURE.md
鈹�   鈹斺攢鈹€ TESTS.md
鈹溾攢鈹€ tests/
鈹�   鈹斺攢鈹€ test_syntax.py
鈹斺攢鈹€ .github/workflows/
    鈹斺攢鈹€ python-check.yml
```

## Licence