# SPORTS IN POLITICS OR POLITICS IN SPORTS?

## View point

The invasion of Ukraine by Russia has multiple collateral damages. Most noticed is on the economic ground with the energy ban and subsequent inflation. But as the Paris Summer Olympics are getting closer, the conflict is becoming increasingly present on the sports front. 

## The Analysis

With recent decisions from the Olympic Committee to accept Russian and Belarus athletes under certain conditions, the topic has hit the press titles.
We include in the analysis articles from the French sport newspaper L’Equipe, the Italian public broadcaster RAI News, a Spanish sport title Estadio Deportivo. To have a different view point, we included the English edition of the Russian Pravda newspaper. All articles were published between December 8th and December 19th 2023.

## Tools

We used two AWS services: the first one, Translate, to get an English version of the articles; the second one, Comprehend, to have a selection of key words and the “sentiment” coming out of these articles.

## Findings

Content
Whilst the French and the Spanish media refer specifically to the war, the Italian media do not as the article is focused on the more opened position of Sebastian Coe, president of World Athletics. As expected, no mention is made on the war, neither on the special operation, on the Russian media.

Sentiment
More revealing is the sentiment analysis, from AWS Comprehend, which illustrates the neutrality in all three western media, as opposed to the negative sentiment expressed in the Russian Pravda (English edition). 

![image](https://github.com/amer1606/DE2_Assign3_AMerceron/assets/144542620/1d90e00e-0b29-45a1-86dc-446574ac96f6)

## The Process

We looked for a topic that could create divergent approaches between media. Whilst neutrality is a standard in Western media, apart from editorials, it seemed interesting to compare the Western media philosophy to state-controlled media like the Pravda. Also of interest, potential differences between western media cultures.

![L'Equipe](https://github.com/amer1606/DE2_Assign3_AMerceron/assets/144542620/f69b1a01-a432-4618-8864-0f1a41c245a8)
In our selection, L’Equipe is the main sport media in the organizing country (where political pressure to make the event successful is important, with possibly French pride playing a role). Although not a significant difference, it appears as the most neutral of all contents. Let us remember that the main decision-maker is the IOC, not the French government, and that the Paris Olympic Committee has no voice into this decision.

![RAI](https://github.com/amer1606/DE2_Assign3_AMerceron/assets/144542620/b2360dfb-c78b-4e4d-aeb1-624120f4371f)
The Italian media from State owned RAI, does not show major biased sentiment in its content (slightly negative sentiment).

![Estadio Deportivo](https://github.com/amer1606/DE2_Assign3_AMerceron/assets/144542620/509939b2-92c1-439c-a83a-240b278a3100)
The Spanish media is a classical Sport content newspaper, not surprisingly not showing sentiment bias.

![Pravda](https://github.com/amer1606/DE2_Assign3_AMerceron/assets/144542620/11c43853-c3f9-4141-9541-1b4797f1b4ec)
Not surprisingly the Russian media is measured by AWS with a substantial negative sentiment with a possible mix of nationalism and political alignment.

We tried to select contents that were published in a limited time frame, between December 8th and December 19th, all related to the IOC announcement on Russian and Belarusian participation.

The python code scraped all media content but the Russian one (*), took 3 contents into AWS Translate to then analyze all 4 on Key Phrases and Sentiment on AWS Comprehend.

Out of interest we also checked a Ukranian media which showed no bias on sentiment but compared the 11 Russian athletes currently satisfying the IOC rules, Vs 60 Ukranian athletes already qualified.
(*): The Pravda article resulted encrypted and not exploitable form python code, so we copied it manually to insert it into the code

## Appendix

### L'EQUIPE - French

Key phrases	/ Confidence
Less than two hours	0.95
the IOC	0.99+
Russian and Belarusian athletes	0.99+
the Paris Olympic Games	0.99+
a neutral banner	0.99+
reactions	0.99+
the Russian media	0.99+
its analysis	0.99+
the daily Sport-Express	0.99+
the card	0.99+

### RAI NEWS - Italian

Entity	Type	Confidence
Russia	Location	0.99+
Belarus	Location	0.99+
2024 Paris Olympic Games	Event	0.94
president	Person	0.59
World Athletics	Organization	0.98
Sebastian Coe	Person	0.99+
Coe	Person	0.99+
five minutes	Quantity	0.75
GettyImages	Organization	0.97
Sebastian Coe	Person	0.99+

### ESTADIO DEPORTIVO

Key phrases	Confidence
The participation	0.99+
Russian athletes	0.99+
the Paris 2024 Olympic Games	0.99+
real headaches	0.99+
the invasion	0.99+
Ukraine	0.99+
subsequent war	0.99+
the situation	0.99+
these athletes	0.99+
a possibility	0.99+

### PRAVDA

Key phrases	Confidence
Russian athletes	0.99+
part	0.99+
2024 Olympic Games 18.12.2023 16:15 Sport	0.94
The head	0.97
the All-Russian Rhythmic Gymnastics Federation	0.99+
Irina Viner	0.99+
her athletes	0.99+
international tournaments	0.99+
a neutral status	0.99+
TASS reports	0.80

## Sentiment Comparison

![image](https://github.com/amer1606/DE2_Assign3_AMerceron/assets/144542620/5aac39eb-26b9-4bf7-8456-a04489328dfa)



