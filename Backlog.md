# SOR Backlog

1. Migrate Market into another project as ExternalMarket

1. To introduce IMarket/Market for indomain use

1. To introduce the concept of (financial) instrument (mandatory to support the concept of *Market data* feeds)

1. To introduce the notion of market data and the MarketData API & Port/Adapter (starting from our acceptance tests)

1. To introduce the *OrderRouting* API & corresponding port/adapter

1. To create our acceptance test harness (i.e. a console application generating a report after each runs session)



## Remarks
+ Null object pattern instead of nulls

+ Implement asynchronous nature of the markets (for their feedback)

+ Try various technical strategy for the inside-the-hexagon implementation (LMAX, F#, Michonne, ...)

+ Conclude and call for action for other guys/languages/platforms...


- - - 

## Events autours du passage d'ordre
Cf photo Cyrille
1, 2, 3, 4 dans presque tous les ordres possibles (race cond fonctionnelles)

1. Order updated: Canceled, executed, ... new status

	1. __Exec notif__: a quel prix tu as trait� effectivement

2. Trade Info (traded):  avec qui? marges y/no ? settlement condition? (sous quels termes)

3. Last traded price: mise � jour du flux (dernier prix trait� par instrument) -> le cours (last executed price)

4. __Feed Updated__: mise � jour du flux, avec impact sur les quantit�s par exemple et les prix 



Le solver est int�ress� par 3 et 4

