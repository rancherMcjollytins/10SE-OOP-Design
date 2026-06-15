# 10SE-OOP-Design
## Top Trumps

### PT1 - STEPTHROUGH PLAN
|Step|x|
|:--:|:--:|
|WHY|x|

---
how this gam ework
### PT2 - Six Attributes
Six attributes for the Top Trumps card game:
|Attribute|Data Type|Description|
|:-------:|:-------:|:---------:|
|Price   |Float    |The market price of the car on the card in **U.S. dollars**, as a 2 point float. For this game, **lower price is better, as it is more affordable**.|
|Horsepower|Int  |The horsepower (hp) of the car.|
|Payload|Float|The maximum amount of weight that the car can carry, in **kilograms**. Higher power to weight is better.|
|Power-Weight Ratio|Float|The ratio of horsepower to weight, **calculated as power (hp) over weight (kg)**|
|Top Speed|Int|Top speed of the car in **kilometres per hour.**|
|Fuel Efficiency/Economy|Float|The distance a car can travel per unit of fuel, calculated as **Liters Per 100 km travelled.**|

These attributes were chosen because they are relevant to a cars system and value, and they are balanced, as specific stats modify the values of others, for example:
* Price
    * If price is set as lower = better, The more a car has in some other stats like power, the more it costs. This means that cars with lower stats will win in the price category.
* Payload vs Power
    * A car with a high horsepower and top-speed, like a supercar, might have a lower payload in comparison to something like a ute or a van.

