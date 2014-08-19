Ubiquitous language
===================
 
- __Order routing:__ is the process by which an order for financial instruments (currencies, securities, commodities, derivatives, futures, options,...) goes from the end user (e.g. trader) to an exchange. An order may go directly to the exchange from the end user, or it may go first to a broker who then routes the order to the exchange.

- __Routing Destination / Execution Venue__: means a broker, a dealer (e.g. bank) or a venue/exchange/market where we can route orders to.

- __"Smart" Order Routing (SOR)__ attempts to achieve best execution of trades while minimizing market impact. SOR automates the selection of execution venues and methodology in order to assure best execution, systematizes the selection process, and reduce execution costs.

*"It is designed to help firms in an increasingly fragmented market to search for hidden liquidity, find opportunities in dark pools and use algorithms to maximize results without moving the market"* (source: [MarketsWiki](http://marketswiki.com/mwiki/Order_routing))

- - -

SOR interfaces
--------------
Traders ask the Smart Order Router (SOR for short) to execute orders of 2 types:

- __Market order:__ simple order (1 leg only?) associated to a given venue/market/exchange

- __Trading order:__ more complex order that is usually transformed by the SOR into a set of Market Orders executed in one or various venues/markets/exchanges. The number of market orders and the choice of their venue depends on the market conditions, affinities that we may have with venues, and the algorithms we enable within the SOR.

- - -

Trading Order types
-------------------

- __Simple order:__ one leg order (always matching with a Market Order?)
- __OCO ([One-Cancels-the-Other Order](http://www.investopedia.com/terms/o/oco.asp)):__ 2 legs order. First leg is a *[Take Profit Order](http://www.investopedia.com/terms/t/take-profitorder.asp)* and the other: a *[Stop Loss Order](http://www.investopedia.com/terms/s/stop-lossorder.asp)*
- __Entry:__ 3 legs [Conditional Order](http://www.investopedia.com/university/intro-to-order-types/conditional-orders.asp). (if entry leg is done ==> OCO)
- __EntryLoop:__ ???
- __TWAP:__ ???


Market Order type(s)
--------------------

- __Spot Simple Order__


Execution strategies of a SOR
-----------------------------
- GTC (Good 'till Cancel)
- IOC (Immediate or Cancel)
- Simple Order

- - - 

Diff�rents concepts:
--------------------
Objectif/intention (du client)
Contrainte d'execution
Algo
Conditions de d�clenchement

SOR <=> un broker (intentions  du client en entr�e, et les executer)
- - -

On donne un prix souhait�, et l'algorithme d'execution
WAP: Waited Average Price
T-WAP: one million every 5 minutes (parce je veux executer 100 et j'ai 2 heures)
V-WAP: volume waited

OCO: strat�gie d'investisseur (client)

Immediate Or Cancel (modalit�)
FOK: Fill or Kill (full exec <=> Full Or Nothing) / ?
Un ordre aux limites = 

le SOR actuel exploite (passe sur les march�s)
Ordre Limite (limit� au prix) avec une strat�gie Immediate Or Cancel or Running

Vis � vis du march�, on n'utilise que des Market Orders et des Limit Orders
Tr�s concr�tement, on cr�� qqchose avec l'API de passage d'ordre
Quantity
Price
Instrument
Running: = LimitORder or immediate
- - - 

Attention: tout n'est pas order dans la liste ci-dessous
Cot� investisseur (e.g. OMS):
T/P: Take Profit
Stop Loss
OCO : TP + SL (mais un sur les deux)
Entry: Ordre d'entr�e + 1 OCO (ssi l'ordre d'entr�e est execut�)
Entry Loop: Entry et je repose un entry � la fin (ad lib?)

SOR exec strategy
---
+ Simple Strategy : cible un seul march� uniquement
+ Sweep Strategy: cible plusieurs march�s.

Important: Un enjeu de risque qui ne peut pas �tre abstrait (d�cision inform�e de l'investisseur)

Notre SOR, va recevoir des intentions en provenance des investisseurs, et les 

Diff�rents types de liquidity providers (cumulatif ou ind�pendant)
EBS/Reuters: march�s d'ordres
sinon aggregators
Pleins de contraintes en fonction des march�s (ex: Reuters: minimum 1 Million)

- - - 

Cycle de vie c�t� client doit �tre diff�rent de celui cot� march� (retry and Co)
















