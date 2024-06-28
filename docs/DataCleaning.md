# Voorbewerking van de Dataset

We hebben gekozen voor de dataset 'City Happiness Index' van Kaggle.com. Deze dataset bevat verschillende kenmerken en metingen van steden wereldwijd, gericht op factoren die de totale geluksscore van elke stad kunnen beïnvloeden. 

[klik hier voor de gebruikte dataset](https://www.kaggle.com/datasets/emirhanai/city-happiness-index-2024?select=train.csv)

## Data Cleaning

Tijdens het uitvoeren van de data cleaning hebben we vastgesteld dat elke stad slechts een enkele meting heeft in de dataset. Dit betekent dat elke stad uniek is en niet meerdere keren voorkomt in de dataset in verschillende jaren of maanden. Om deze reden hebben we de kolommen **Month** en `Year` uit de dataset verwijderd, omdat deze informatie niet relevant is voor onze analyse. Daarnaast hebben we de kolom <strong> 'Traffic_Density' </strong> verwijderd, aangezien we deze variabele niet zullen gebruiken in ons onderzoek.

Verder zijn er in deze dataset geen ontbrekende waarden aangetroffen, wat betekent dat de dataset op dit punt onveranderd is gebleven.

## Variable descriptions

In terms of variable type and measurement scale, the variables in the final
dataset can be classified under several combinations:

- Continuous / Ratio variables: `YearsCode`, `YearsCodePro`, `Salary`
- Discrete / Ordinal variables: `JobSat`
- Discrete / Nominal variables: `Education`, `OrgSize`, `LastNewJob`,
  `Employment`, `RespondentType`, `JobSeek`, `Gender`, `Student`, `Country`,
  `CodingActivities`, `DevType`, `LearnCodeFrom`, `LangPresent`
- Discrete / Interval variables: `Year`
- Discrete / Ratio variables: `Age`

Variables that are currently being used are: `Year`, `Salary`, `YearsCodePro`,
`Age`, `Education`, `RespondentType`, `Gender`, `Country` and `DevType`.

## Aggregations

In general, most aggregations happen for calculating the salary gap between men
and women relative to men. This is done by taking the mean salary for both men
and women, subtracting these means and finally divide the total by the mean
salary for men. In mathematical notation, this is defined as:

$$\textrm{SalaryGap} = \frac{S_{\textrm{man}} - S_{\textrm{woman}}}{S_{\textrm{man}}}$$

In most graphs a percentage is being used, which is the above salary gap formula
multiplied by 100.

**Example:** Let's say in the Netherlands the average annual salary for men is
&euro;80,000 and for women &euro;60,000. Then the salary gap will be 25% using
the aforementioned calculation. If women are the ones making &euro;80,000 per
year and men make &euro;60,000 per year, then the salary gap will be -33%. We
call the percentage outcome a *male-favoured gap* if the percentage is positive.
When the outcome is negative, it is considered a *female-favoured gap*.