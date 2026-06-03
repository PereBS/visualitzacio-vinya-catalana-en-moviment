# Fitxers preparats per a Observable

Aquesta carpeta conté els fitxers CSV i el fitxer GeoJSON que carrega directament la visualització publicada a Observable.

Aquests fitxers no són dades originals, sinó versions preparades específicament per simplificar el codi JavaScript de la visualització. La preparació prèvia permet separar la fase de tractament de dades de la fase de disseny visual i interactivitat.

## Funció d'aquests fitxers

Els fitxers d'aquesta carpeta s'utilitzen per construir les diferents escenes de la visualització:

```text
P1 · Reconfiguració territorial
  Mapes, evolució de superfície i fases temporals.

P2 · Transformació varietal
  Rànquings varietals, activitat registral i comparació territorial.

P3 · Clima i rendiment
  Anys crítics, indicadors climàtics i relació exploratòria amb el rendiment.
```

## Fitxers geogràfics

El fitxer GeoJSON de comarques s'utilitza per construir els mapes territorials de la visualització.

## Relació amb els datasets processats

Els fitxers d'aquesta carpeta deriven dels datasets processats situats a:

```text
data/processed/
```

Els datasets processats documenten la base analítica del projecte, mentre que els fitxers d'aquesta carpeta estan adaptats per ser llegits directament per Observable.

## Nota metodològica

Aquesta separació evita carregar tota la preparació de dades dins del notebook Observable.

Observable s'utilitza principalment per:

* carregar fitxers ja preparats;
* construir mapes i gràfics;
* gestionar selectors i interactivitat;
* comunicar visualment els resultats.

Els càlculs principals, les agregacions i els rànquings s'han fet prèviament en la fase de preparació de dades.

