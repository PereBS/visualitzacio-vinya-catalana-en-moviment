# Visualització Observable

Aquesta carpeta conté informació relacionada amb la visualització publicada a Observable.

La visualització principal del projecte es desenvolupa a Observable Notebook i s'ha plantejat com una narrativa interactiva sobre la reconfiguració recent de la vinya catalana entre 2008 i 2024.

## Enllaç a la visualització

https://observablehq.com/d/846746cc9be151d1

## Dades utilitzades per Observable

Els fitxers CSV i el GeoJSON que carrega directament la visualització es troben a:

```text
data/observable_ready/
```

Aquesta carpeta inclou els fitxers preparats per construir les escenes principals de la visualització:

```text
P1 · Reconfiguració territorial
P2 · Transformació varietal
P3 · Clima i rendiment
```

## Separació entre dades i visualització

Observable s'utilitza principalment per:

* construir mapes, gràfics i components visuals;
* gestionar selectors i interactivitat;
* presentar la narrativa visual del projecte;
* facilitar l'exploració dels resultats.

La preparació de dades, les agregacions principals i els rànquings s'han fet prèviament. Aquesta decisió permet reduir la complexitat del codi JavaScript i separar la fase de tractament de dades de la fase de visualització.

## Documentació relacionada

La metodologia i les fonts de dades es documenten a:

```text
docs/nota_metodologica.md
docs/fonts_dades.md
```

Els datasets processats principals es troben a:

```text
data/processed/
```

## Exportació

En cas que s'inclogui una exportació del notebook Observable, aquesta es guardarà en aquesta carpeta.
