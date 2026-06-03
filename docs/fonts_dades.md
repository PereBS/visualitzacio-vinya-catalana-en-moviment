# Fonts de dades

Aquest projecte utilitza dades públiques i fitxers derivats preparats específicament per analitzar la reconfiguració recent de la vinya catalana entre 2008 i 2024.

La visualització s'estructura en tres blocs:

```text
P1 · Reconfiguració territorial
P2 · Transformació varietal
P3 · Clima i rendiment
```

## 1. Estadístiques definitives de conreus

Font principal per a les dades de superfície, producció i rendiment de la vinya per comarca i any.

**Institució:** Generalitat de Catalunya. Departament d'Acció Climàtica, Alimentació i Agenda Rural.

**Ús en el projecte:**

* superfície productiva de vinya per comarca;
* producció total de raïm per a vi;
* rendiment productiu;
* evolució territorial entre 2008 i 2024;
* construcció del panell comarcal-anual.

**Relació amb la visualització:**

Aquesta font és la base principal de la pregunta P1, centrada en la reconfiguració territorial de la vinya catalana.

També s'utilitza a P3 per relacionar rendiment productiu i context climàtic.

## 2. Servei Meteorològic de Catalunya

Font utilitzada per construir la capa climàtica del projecte.

**Institució:** Servei Meteorològic de Catalunya.

**Fitxer inclòs al repositori:**

```text
data/processed/meteocat_stations_1950_2024.csv
```

**Ús en el projecte:**

A partir de les dades meteorològiques mensuals s'han construït indicadors climàtics anuals i estacionals, com ara:

* precipitació anual;
* recàrrega hídrica hivernal;
* precipitació de primavera;
* temperatura màxima mitjana anual;
* temperatura màxima mitjana de juny-agost;
* temperatura màxima mitjana de juliol-agost.

**Relació amb la visualització:**

Aquesta font és la base climàtica de la pregunta P3, centrada en la relació exploratòria entre clima i rendiment productiu.

## 3. Registre Vitivinícola de Catalunya eRVC

Font complementària utilitzada per estudiar activitat registral varietal i indicis de renovació estructural.

**Institució:** Generalitat de Catalunya.

**Fitxer de base inclòs al repositori:**

```text
data/processed/Registre_Vitivin_cola_de_Catalunya__e-RVC_.csv
```

**Fitxer derivat principal:**

```text
data/processed/p2_comarca_varietat_2008_2024_enriched.csv
```

**Ús en el projecte:**

* identificació de varietats registrades;
* agregació per comarca i varietat;
* anàlisi de modificació varietal documentada;
* comparació territorial de l'activitat registral.

**Relació amb la visualització:**

Aquesta font és la base de la pregunta P2, centrada en la transformació varietal i la renovació estructural.

## Advertiment sobre l'eRVC

La informació procedent del Registre Vitivinícola de Catalunya té naturalesa registral.

Per aquest motiu, en aquest projecte no s'interpreta com:

* hectàrees úniques;
* estoc productiu real;
* noves plantacions netes;
* mesura directa de superfície productiva agregada.

S'interpreta com a activitat registral o modificació varietal documentada.

## 4. Atles climàtic de Catalunya 1991–2020

Font de contrast utilitzada en la revisió metodològica de la reconstrucció proxy de les variables tèrmiques.

**Institució:** Servei Meteorològic de Catalunya.

**Ús en el projecte:**

* contrast territorial de la plausibilitat climàtica;
* suport a la selecció de comarques proxy;
* revisió de casos dubtosos en la cobertura tèrmica.

**Relació amb la visualització:**

Aquesta font no es carrega directament a Observable, però ajuda a justificar la construcció del dataset proxy utilitzat en P3.

## 5. Fitxers derivats del projecte

A més de les fonts originals, el repositori inclou fitxers derivats i preparats per a la visualització.

Els datasets processats principals es troben a:

```text
data/processed/
```

Els fitxers que carrega directament Observable es troben a:

```text
data/observable_ready/
```

Aquesta separació permet distingir entre:

* fonts de base;
* datasets processats;
* fitxers preparats específicament per a la visualització;
* documentació metodològica.

## Nota sobre llicències i ús acadèmic

El codi del projecte es publica sota llicència MIT.

Les dades originals provenen de fonts públiques oficials. Els fitxers inclosos en aquest repositori són versions derivades o preparades amb finalitat acadèmica i de reproducció de la visualització.

Les fonts originals mantenen les seves pròpies condicions d'ús.
