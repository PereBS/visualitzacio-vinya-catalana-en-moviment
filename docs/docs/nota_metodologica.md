# Nota metodològica

Aquest projecte analitza la reconfiguració recent de la vinya catalana entre 2008 i 2024 a partir de dades de superfície, producció, rendiment, clima i activitat registral varietal.

La visualització s'estructura en tres preguntes principals:

1. **P1 · Reconfiguració territorial**
   Analitza com ha canviat la superfície productiva de vinya per comarca entre 2008 i 2024.

2. **P2 · Transformació varietal i renovació estructural**
   Utilitza el Registre Vitivinícola de Catalunya com a font complementària per estudiar l'activitat registral associada a varietats i territoris.

3. **P3 · Clima i rendiment productiu**
   Contextualitza els anys de baix rendiment a partir d'indicadors climàtics de precipitació, recàrrega hídrica i temperatura màxima estival.

## Separació entre preparació de dades i visualització

La preparació de dades s'ha fet abans de construir la visualització final.

Observable carrega principalment fitxers CSV ja preparats, situats a:

```text
data/observable_ready/
```

Aquesta decisió permet:

* reduir la complexitat del codi JavaScript;
* separar el tractament de dades del disseny visual;
* facilitar la lectura del notebook;
* evitar càlculs repetitius dins de la visualització;
* millorar la traçabilitat dels resultats.

Els datasets de base i processats es troben a:

```text
data/processed/
```

## Dataset strict

El fitxer:

```text
viticultura_clima_strict.csv
```

conté el panell comarcal-anual amb dades de superfície, producció, rendiment i clima, mantenint la informació climàtica directa quan existeix cobertura disponible per comarca i any.

Aquesta versió ofereix una lectura més conservadora de les dades, però presenta buits en algunes variables climàtiques, especialment les tèrmiques.

## Dataset proxy

El fitxer:

```text
viticultura_clima_proxy_v2.csv
```

és la versió analítica final utilitzada per ampliar la cobertura de les variables de temperatura.

La reconstrucció proxy s'aplica a variables tèrmiques, no a la precipitació. La correspondència entre comarques sense cobertura directa completa i comarques font es documenta al fitxer:

```text
proxy_comarques_temperatura.csv
```

Aquesta versió permet una lectura més completa de la relació exploratòria entre clima i rendiment, però no s'ha d'interpretar com a observació climàtica directa en tots els casos.

## Dades meteorològiques

El fitxer:

```text
meteocat_stations_1950_2024.csv
```

conté la base meteorològica utilitzada per construir indicadors climàtics anuals i estacionals.

A partir d'aquestes dades s'han generat variables com:

* precipitació anual;
* recàrrega hídrica hivernal;
* precipitació de primavera;
* temperatura màxima mitjana anual;
* temperatura màxima mitjana de juny-agost;
* temperatura màxima mitjana de juliol-agost.

Aquests indicadors s'utilitzen com a aproximacions exploratòries i no com a mesures completes del balanç hídric real de la planta.

## Capa eRVC

El fitxer:

```text
Registre_Vitivin_cola_de_Catalunya__e-RVC_.csv
```

conté la font de base del Registre Vitivinícola de Catalunya.

Aquesta capa s'utilitza com a font complementària per analitzar activitat registral varietal. No s'interpreta com a recompte exacte d'hectàrees úniques, estoc productiu real o noves plantacions netes.

El fitxer:

```text
p2_comarca_varietat_2008_2024_enriched.csv
```

és una versió agregada i enriquida derivada de l'eRVC, utilitzada per construir les visualitzacions de la pregunta P2.

## Interpretació climàtica

Els indicadors climàtics s'utilitzen amb finalitat exploratòria.

La visualització no pretén demostrar causalitat estricta entre clima i rendiment, sinó identificar patrons i associacions plausibles entre:

* recàrrega hídrica hivernal;
* precipitació de primavera;
* temperatura màxima estival;
* rendiment productiu anual.

## Limitacions principals

Les principals limitacions del projecte són:

* les variables climàtiques no capturen tot el balanç hídric real de la planta;
* no s'inclouen variables com evapotranspiració, humitat del sòl o episodis extrems detallats;
* l'eRVC té naturalesa registral i no equival a una mesura directa de superfície productiva real;
* la visualització és exploratòria i no causal;
* les dades no permeten incorporar una anàlisi empírica de perspectiva de gènere.

## Relació amb la visualització final

La visualització publicada a Observable utilitza fitxers preparats per construir una narrativa visual en tres blocs:

```text
P1 · Reconfiguració territorial
P2 · Transformació varietal
P3 · Clima i rendiment
```

Aquesta estructura manté la coherència amb les preguntes de recerca definides a la primera part de la pràctica.
