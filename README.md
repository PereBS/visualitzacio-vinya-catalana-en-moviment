# Visualització: La vinya catalana en moviment

Projecte final de l'assignatura **Visualització de dades**.

Aquesta visualització analitza la reconfiguració recent de la vinya catalana entre 2008 i 2024, combinant dades de superfície vitícola, producció, rendiment, clima i informació complementària del Registre Vitivinícola de Catalunya.

## Enllaç a la visualització

Pendent d'afegir l'enllaç públic a Observable.

## Objectiu del projecte

El projecte vol respondre tres preguntes principals:

1. **Reconfiguració territorial**  
   Com ha canviat la distribució de la superfície productiva de vinya per comarca entre 2008 i 2024?

2. **Transformació varietal i renovació estructural**  
   Quines varietats concentren més activitat registral al Registre Vitivinícola de Catalunya i en quins territoris?

3. **Clima i rendiment productiu**  
   Com es poden contextualitzar els anys de baix rendiment a partir d'indicadors climàtics com la precipitació i la temperatura màxima estival?

## Fonts de dades

El projecte combina diferents fonts públiques i dades preparades específicament per a la visualització:

- Estadístiques definitives de conreus de la Generalitat de Catalunya.
- Dades climàtiques mensuals del Servei Meteorològic de Catalunya.
- Registre Vitivinícola de Catalunya, utilitzat com a font complementària per a l'anàlisi varietal.
- Fitxers derivats i preparats per a Observable.

## Estructura del repositori

```text
data/
  processed/          Datasets processats principals
  observable_ready/   CSV preparats específicament per a la visualització

docs/
  notes metodològiques i documentació del projecte

observable/
  exportació o fitxers relacionats amb la visualització Observable
```

## Nota metodològica

Els fitxers `observable_ready` no són dades originals, sinó versions preparades per simplificar el codi JavaScript d'Observable. Els càlculs principals s'han fet prèviament per separar la preparació de dades de la visualització.

La capa del Registre Vitivinícola de Catalunya s'interpreta com a activitat registral i no com a recompte exacte d'hectàrees úniques, estoc productiu real o noves plantacions netes.

Els indicadors climàtics s'utilitzen amb finalitat exploratòria. La visualització no pretén demostrar causalitat estricta entre clima i rendiment, sinó contextualitzar patrons territorials i anys crítics.

## Llicència

El codi d'aquest projecte es publica sota llicència MIT.

Les dades originals provenen de fonts públiques oficials. Els fitxers inclosos en aquest repositori són versions derivades o preparades per a ús acadèmic i per a la reproducció de la visualització.

docs/
  notes metodològiques i documentació del projecte

observable/
  exportació o fitxers relacionats amb la visualització Observable
