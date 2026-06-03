# Visualització: La vinya catalana en moviment

Projecte final de l'assignatura **Visualització de dades**.

Aquesta visualització analitza la reconfiguració recent de la vinya catalana entre 2008 i 2024, combinant dades de superfície vitícola, producció, rendiment, clima i informació complementària del Registre Vitivinícola de Catalunya.

## Enllaç a la visualització

[Obrir la visualització a Observable](https://observablehq.com/d/846746cc9be151d1)

## Objectiu del projecte

El projecte vol respondre tres preguntes principals:

1. **Reconfiguració territorial**
   Com ha canviat la distribució de la superfície productiva de vinya per comarca entre 2008 i 2024?

2. **Transformació varietal i renovació estructural**
   Quines varietats concentren més activitat registral al Registre Vitivinícola de Catalunya i en quins territoris?

3. **Clima i rendiment productiu**
   Com es poden contextualitzar els anys de baix rendiment a partir d'indicadors climàtics com la precipitació, la recàrrega hídrica i la temperatura màxima estival?

## Fonts de dades

El projecte combina diferents fonts públiques i dades preparades específicament per a la visualització:

* Estadístiques definitives de conreus de la Generalitat de Catalunya.
* Dades climàtiques mensuals del Servei Meteorològic de Catalunya.
* Registre Vitivinícola de Catalunya, utilitzat com a font complementària per a l'anàlisi varietal.
* Fitxers derivats i preparats per a Observable.

## Estructura del repositori

```text
data/
  processed/          Datasets processats i fonts de base
  observable_ready/   CSV i GeoJSON preparats específicament per a Observable

docs/
  nota_metodologica.md
  fonts_dades.md

observable/
  informació o exportació relacionada amb la visualització Observable
```

## Documentació

La documentació principal del projecte es troba a la carpeta `docs/`:

* `docs/nota_metodologica.md`: explica la construcció dels datasets, la diferència entre les versions strict i proxy, el tractament de l'eRVC i les limitacions principals.
* `docs/fonts_dades.md`: resumeix les fonts de dades utilitzades i la seva funció dins del projecte.

La carpeta `data/processed/` conté els datasets principals i fonts de base utilitzats en la preparació analítica.

La carpeta `data/observable_ready/` conté els fitxers que carrega directament la visualització d'Observable.

## Nota metodològica

Els fitxers `observable_ready` no són dades originals, sinó versions preparades per simplificar el codi JavaScript d'Observable. Els càlculs principals s'han fet prèviament per separar la preparació de dades de la visualització.

La capa del Registre Vitivinícola de Catalunya s'interpreta com a activitat registral i no com a recompte exacte d'hectàrees úniques, estoc productiu real o noves plantacions netes.

Els indicadors climàtics s'utilitzen amb finalitat exploratòria. La visualització no pretén demostrar causalitat estricta entre clima i rendiment, sinó contextualitzar patrons territorials, varietals i productius.

## Llicència

El codi d'aquest projecte es publica sota llicència MIT.

Les dades originals provenen de fonts públiques oficials. Els fitxers inclosos en aquest repositori són versions derivades o preparades per a ús acadèmic i per a la reproducció de la visualització.

Les fonts originals mantenen les seves pròpies condicions d'ús.
