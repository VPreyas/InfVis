# Dataset and Preprocessing

We hebben gekozen voor de dataset 'City Happiness Index' van Kaggle.com. Deze dataset bevat verschillende kenmerken en metingen van steden wereldwijd, gericht op factoren die de totale geluksscore van elke stad kunnen beïnvloeden. 

[klik hier voor de gebruikte dataset](https://www.kaggle.com/datasets/emirhanai/city-happiness-index-2024?select=train.csv)

## Data Cleaning

Tijdens het uitvoeren van de data cleaning hebben we vastgesteld dat elke stad slechts een enkele meting heeft in de dataset. Dit betekent dat elke stad uniek is en niet meerdere keren voorkomt in de dataset in verschillende jaren of maanden. Om deze reden hebben we de kolommen `Month` en `Year` uit de dataset verwijderd, omdat deze informatie niet relevant is voor onze analyse. Daarnaast hebben we de kolom `Traffic_Density' verwijderd, aangezien we deze variabele niet zullen gebruiken in ons onderzoek.

Verder zijn er in deze dataset geen ontbrekende waarden aangetroffen, wat betekent dat de dataset op dit punt onveranderd is gebleven.

## Omschrijving van de variabelen

### Discrete Variabele / Nominale schaal

- `City`: De naam van de stad waarin de metingen zijn gedaan.

### Continue Variabele / Ratio schaal

- `Decibel_Level`: Het geluidsniveau in de stad, gemeten in decibel.
- `Green_Space_Area`: Het percentage van het stedelijk gebied dat uit groene ruimte bestaat.
- `Air_Quality_Index`: Een index die de kwaliteit van de lucht in de stad aangeeft.
- `Healthcare_Index`: Een index die de kwaliteit van de gezondheidszorg in de stad aangeeft.
- `Cost_of_Living_Index`: Een index die de kosten van levensonderhoud in de stad weergeeft in vergelijking met een referentiestad.

### Continue Variabele / Ordinale schaal

- `Happiness_Score`: De gemiddelde score die het geluk van de inwoners van de stad aangeeft van 1 - 10. (De Happiness Score wordt beschouwd als een ordinale variabele omdat het de rangorde van geluk aangeeft zonder exact meetbare intervalafstanden tussen scores. Hoewel hogere scores een hoger geluksniveau aangeven, is het niet mogelijk om te zeggen dat een score exact twee keer zoveel geluk vertegenwoordigt als een score die de helft ervan is.
