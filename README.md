# Code Poker

Code Poker is a social programming game for 3-10 players.

Before the game, each player will prepare a short programming challenge that
the other players will be tasked with solving in the fewest lines of code.

At the beginning of every round, a random player will be selected,
who will present their pre-prepared coding challenge.
Then, each player will secretly write down the number of lines of code they
believe they can complete the challenge in. After concluding the bidding, the coding phase begins.

Players have 10-15 minutes to complete the programming challenge.
The round is won by whoever bid the lowest and completed the challenge within the number of lines they bid. 
> **Example:**
>
> Player One presents their coding challenge: to reverse a linked list (how boring).
>
> After presenting the challenge, bidding begins. 
> Simultaneously, Player One secretly bids 5 lines, and Player Two secretly bids 7 lines.
>
> The coding phase commences, and Player One finishes in exactly 5 lines, and Player Two finishes in 4.
>
> Even though Player Two finished in fewer lines, Player One had the lower bid, so Player One wins the round. If Player One was unable to complete the challenge, Player Two would have won.  

## The Testing Phase

After the coding phase ends, all players who successfully
completed the challenge will randomly pass their code to another player for judging.

The judging player has five minutes to generate one test case and test it against the program they have been given. If the code passes the test, it is considered to have passed the challenge.

> Test cases should be comprehensive, but fair. 
> Test cases should not contain empty or malformed input, though they are encouraged to be as devious and targeted as possible. Half of the fun finding any opening in your opponent's program!

## Ending the Round - Language Selection

The winner of the first round chooses the language that
all players must use for the next round.

Players may choose to play on-language, using that language to write their program, or play off-language.

A player who plays off-language is ineligible to win the round. Only programs which use the declared language may win.

However, the off-language player who completes the challenge with the lowest bid will begin the Language Selection Phase at the end of a round.

When ending a round other than the first, the Language Selection phase begins. The off-language player who completed the challenge with the lowest bid declares the language for the next round. In clockwise order, players have the option to change the language or pass. To change the language, a player must accept a 5-line penalty, which increases by 5 for each language change which has already happened. 
> **Example:**
>
> Player One wins the first round, and declares Haskell as the language for the next round
>
> Player Two doesn't know haskell, so they elect to play off-language by writing their solution in JavaScript, and successfully complete the challenge with the lowest bid of all of the other off-language players.
>
> Player Two, having done the best of all of the off-language players, declares JavaScript (their favorite!) as the next language.
> 
> Then, the player to Player Two's left is given the opportunity to change the language by accepting a 5-line penalty on the next round.
> 
> Player Three passes, giving the opportunity to Player Four.
> Player Four accepts a 5-line penalty to change the language to Python.
>
> Next, Player Five has the opportunity to change the language. They do not like Python, so they accept a 10-line penalty to change the language to C++.
>
> Players Six and Seven pass, and it comes back around to Player One, which ends the Language Selection Phase.
>
> The next challenge is presented. Player Four has +5 lines added to their solution's score, and Player Five has +10 lines added to their solution's score for that round.
>
> Player Seven happens to perform the best of the off-language players for that round, and begin the subsequent Langugae Selection Phase.

## Winning

Whichever player wins the most rounds wins that game of Code Poker, accomplished by solving the most challenges with the lowest bid in the declared language for those rounds.

