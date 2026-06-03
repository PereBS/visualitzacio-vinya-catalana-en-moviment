# Carpeta `data`

Aquesta carpeta conté els fitxers de dades utilitzats en el projecte de visualització **La vinya catalana en moviment**.

Les dades s'organitzen en dues subcarpetes principals:

```text
processed/
  Datasets processats i fonts de base utilitzats com a base analítica del projecte.

observable_ready/
  Fitxers CSV i GeoJSON preparats específicament per ser carregats per Observable.
```

## Estructura

### `processed/`

Conté els datasets principals utilitzats per preparar l'anàlisi:

* panell vitícola-climàtic en versió strict;
* panell vitícola-climàtic en versió proxy;
* dades meteorològiques de base;
* fitxer de correspondència dels proxies de temperatura;
* informació de base i derivada del Registre Vitivinícola de Catalunya.

Aquests fitxers permeten documentar la traçabilitat entre les fonts originals i els fitxers finals utilitzats a la visualització.

### `observable_ready/`

Conté els fitxers que carrega directament la visualització d'Observable.

Aquests fitxers ja estan preparats per construir les diferents escenes del projecte:

```text
P1 · Reconfiguració territorial
P2 · Transformació varietal
P3 · Clima i rendiment
```

## Nota metodològica

Els fitxers d'aquesta carpeta són versions processades o derivades de fonts públiques oficials.

Els fitxers de `observable_ready/` no són dades originals, sinó versions preparades per simplificar el codi JavaScript d'Observable i separar la preparació de dades de la visualització.

La informació del Registre Vitivinícola de Catalunya s'utilitza com a activitat registral i no com a recompte exacte d'hectàrees úniques, estoc productiu real o noves plantacions netes.

