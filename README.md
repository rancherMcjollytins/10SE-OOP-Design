# 10SE-OOP-Design
## Top Trumps

### PT1 - STEPTHROUGH PLAN

---
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

---
### PT3 - Class Design
![Class Diagram](Images\partb-evenbetter.png)
|Class|Description|Relationships|
|:---:|:---------:|:-----------:|
|Game |Game that has players, deck, and round that play until the game ends. The game methods allow it to begin a game, play and loop rounds, and work out winners/draws or game overs.  |1 Game has 1 deck. 1 Game has 2 to 4 players.            |
|Deck |A deck of cards that deals to players. The deck's methods allow it to be shuffled, allow it to deal cards and allow players to remove cards from the deck and add it to their hand.           |1 Deck can have 1 to  many cards.            |
|Player|A player in the game. Can get and can play cards/card attributes. Has a hand of cards (dealt by the deck) and can win the game by getting the most score (via getting the most cards). Can also draw from deck, and give cards when the rules dictate so.|1 Player can have 1 to many Cards (Ignore Diagram).|
|Card |A card. It makes up the deck and player hands. The card mainly acts as a 'holder' for the car with it's attributes. Can be flipped.     |1 Card has 1 Car.             |
|Car  |A car. It exists as as a part of the card, and contains attributes that will determine which player will win the round. Attributes include price, horsepower, power-weight ratio, top speed, payload, and fuel-economy.          |1 Card has 1 Car. |

---
### PT4 - UML Class Diagram
![UML V1](Images\UML.png)
*Although not shown, players also have points.*

---
### PT5 - Structure Charts and Game Mechanics
![StructureChart](Images\Struc-Chart.png)
#### Game Balancing and Mechanics
Top Trumps is a simple card game that follows a small set of rules:
- At the start of the game, the deck is refilled, shuffled, and an equal amount of cards is dealt to each player.
- The game functions in rounds. For each round, one player selects an attribute of their top card.
- The player then reads out their attribute value. The opposing players reads out their card value.
- Whoever has the highest attribute value wins the opponents card.
- The winner of the round chooses the attribute and begins the next round.
- When one player has all cards, the game ends, and they win.

Balancing follows a system of equal distribution of card values. Depending on the card a player has, different attributes are higher or lower, e.g. A supercar has high horsepower and top speed, but lower payload and greater price, whereas a ute would have low top speed and a lesser power-weight ratio, but a high payload.

One possible issue in balancing could include the presence of 'unfair' attributes, being those more powerful than others, like price.

This could be fixed using a system where price is more effective at lower levels, as raising other attributes will likely increase price, thus resulting in a payoff.

---
### PT6 - Interface and Card Design
#### Card Sketch
![Card Design](Images\Card1.png)
#### Rough UI Sketch
![UI Wireframe](Images\Wireframe-Updated.png)
|Item|Description|
|:--:|:---------:|
|A   |The deck of unrevealed cards that deals to players, and can be drawn from.|
|B   |The amount of points of the player, which increases the more cards you have, and determines the winner at the end of the game.           |
|C   |The round of the game that is currently playing. Loops and adds when a new round occurs.           |
|D   |The cards in a players hand. Consist of multiple components: *D1 -* Card (Holds a car, with images and other design), and *D2 -* Car (Holds attributes and information).|
|E   |Empty slot where players can show their cards, which allows them to compare card to opponents|
|F   |Quit Button if game must be ended early.  |
|G            |Opponents hand draw, which does not show their cards, but does show the amount of cards they hold.           
|H   |Slot for opponent to play their card.|

---
### PT7 - Social, Legal, Ethical Concerns
#### Social
    essay here
#### Legal
    essay here
#### Ethical
    essay here