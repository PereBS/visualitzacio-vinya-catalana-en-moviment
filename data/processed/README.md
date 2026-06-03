# Datasets processats i fonts de base

Aquesta carpeta conté els datasets principals utilitzats per construir la visualització sobre la reconfiguració de la vinya catalana entre 2008 i 2024.

Els fitxers inclosos permeten documentar la traçabilitat entre les fonts de dades, la preparació analítica i els CSV finals utilitzats per Observable.

## Fitxers inclosos

```text
viticultura_clima_strict.csv
  Panell comarcal-anual amb dades de superfície, producció, rendiment i clima.
  Manté la informació climàtica directa quan existeix cobertura disponible per comarca i any.
  Aquesta versió serveix com a base més conservadora del projecte.

viticultura_clima_proxy_v2.csv
  Versió analítica final del panell.
  Incorpora una reconstrucció proxy de les variables tèrmiques per a comarques sense cobertura directa completa.
  És el dataset principal utilitzat per a l'anàlisi exploratòria de clima i rendiment.

proxy_comarques_temperatura.csv
  Taula de correspondència utilitzada per documentar el proxy tèrmic.
  Indica quina comarca font s'ha utilitzat per completar la cobertura de temperatura en les comarques sense dades directes completes.

meteocat_stations_1950_2024.csv
  Dades meteorològiques de base procedents del Servei Meteorològic de Catalunya.
  S'han utilitzat per construir indicadors climàtics anuals i estacionals.

Registre_Vitivin_cola_de_Catalunya__e-RVC_.csv
  Fitxer de base del Registre Vitivinícola de Catalunya.
  S'utilitza com a font complementària per a l'anàlisi de composició varietal i activitat registral.
  La informació d'aquest registre no s'interpreta com a hectàrees úniques ni com a estoc productiu real.

p2_comarca_varietat_2008_2024_enriched.csv
  Dataset agregat i enriquit derivat de l'eRVC.
  Resumeix la modificació varietal documentada entre 2008 i 2024 per comarca i varietat.
  Aquest fitxer serveix de base per a les visualitzacions de la pregunta P2.
