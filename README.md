# Python-Games
## TOURNAMENT GAME GENERATOR
For this project you will be asked to create a program that can schedule games that teams will play in an end of year tournament. You will only be responsible for determining the games played in the first round of the tournament.

You will first need to ask the user of your program to input the number of teams; you may assume there will always be an even number of teams (you don't need to validate this). Next you will need to ask for the names of all of the teams and store them in some way.

After this you'll need to determine the number of games that were played by each team; you may assume each team plays the same number of games. Finally, you'll need to determine the number of wins each team had during the regular season.

When asking for user input, you'll need to make sure all input is valid and ask the user to try again if they give you invalid input. You may assume user input will always be the correct type (i.e. if you ask for a number you will always get an integer). You can determine if the input is invalid by looking at the following constraints:

There are always at least 2 teams in the tournament.
Each team plays every other team at least once in the regular season.
All team names contain at most 2 words and at least 2 characters.
Each team has at minimum 0 wins and no more wins than the number of games they played.
In the first round of the tournament the teams with the most regular season wins play the teams with the least regular season wins. For example, if Team A has 5 wins, Team B has 4 wins, Team C has 3 wins and Team D has 2 wins then Team A and Team D play each other and Team B and C play each other. If teams are tied for wins and/or losses then your program can choose any appropriate team.

Your program should output the games that should be played in the format seen below. The first game outputted should contain the team with the most regular season wins, the second game should contain the team with the second most regular season wins, etc. The home team of each game should be the team with the least wins of the two, if there is a tie in wins your program can chose any appropriate team.


## BLACKJACK CARD GAME

For this project you will be asked to create a simple version of the very popular casino game, Blackjack (also known as 21). You will need to use Object Oriented Programming concepts to implement the logic for creating a deck, dealing cards, shuffling, betting and more. You will not need to implement rules including splitting, doubling down and insurance.

For this Blackjack game there will be two players, the program user and the dealer. The program user will be playing against the dealer to try to accumulate as much money as possible. For simplicity, we will call the program user the "player".

The objective of Blackjack is to end the hand/round with a hand that has a higher value than the hand the dealer has, without going over 21. The value of your hand is determined by the cards in it. Any face card (King, Queen or Jack) is given a value of 10, an ace can have a value of 1 or 11 (whichever benefits you more) and all other cards have a value equal to their number (i.e. all threes have a value of 3). For example, if you have a hand containing a three, two, king and ace your hand has a value of 16; in this case the ace is treated at 1 because if it were to be treated as 11 you would have 26 and be over 21. If at any point the value of your hand is over 21 you immediately lose, and your bet is lost, this is called a bust.

Each hand/round of Blackjack is played as follows. The player places a bet, in this case any amount between 1 and the amount of money they currently have. Next, two cards are dealt to both the player and the dealer, the player has their cards dealt face up while the dealer has one card dealt face up and one dealt face down. It is then the players turn to decide if they would like to hit or stay. If they decide to hit, they will be dealt another card, they may hit as many times as they'd like until the value of their hand exceeds 21, in which case they bust and lose the hand. If a player decides to stay then their turn is over and the value of their hand is locked, they may stay at any point during their turn.

Once the players turn is over the dealer will flip over their face down card and hit or stay according to a set of rules.

If their hand has a value of 17 or more they must stay.
If their hand has a value of 16 or less they must hit.
The dealer must continue to hit until their hand has a value of 17 or greater, if the value of their hand ever exceeds 21, they immediately lose.
Once the dealer stays or busts the hand/round is over and the winner is decided by the player with the hand that has the highest value not exceeding 21.

If the player is the winner their bet is doubled and returned to them.
If the dealer is the winner they take the players bet.
If the player and dealer tie, then the original bet is returned to the player.
In addition, a special rule in Blackjack is that if a player is dealt a hand with a value of 21 this is considered a natural or "blackjack". If the player has a natural and the dealer does not the dealer pays the player one and a half times their original bet and the hand is immediately over. For example, if the player is dealt an ace and a ten and bet $10, they would be paid $15 and have their $10 returned, ending the hand with $25. However, this is only the case if the dealer does not have a natural as well. If both the player and the dealer have a natural it is a tie, and the bet is returned to the player.

For this game the player will start with $500, and the minimum bet will be $1. Before asking the player to bet you should ask them if they would like to play a hand. If they decide to not play the current hand the game should end and tell the player how much money they left with. If the player ever has $0 the game should end and would have to be restarted for the player to try again. Before each hand all cards should be returned to the deck and the deck should be shuffled.

For this game we will use one deck of 52 cards having 4 suits and 13 cards within each suit (2 - 9, King (K), Queen (Q), Jack (J), Ten (T), Ace (A)). To represent the suits of cards you can use some special Python unicode values. These will only work in Python version 3 and may not work on all operating systems.
