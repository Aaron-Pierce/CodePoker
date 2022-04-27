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
> Test cases should not contain empty or malformed input, though they are encouraged to be as devious and targeted as possible. Half of the fun is finding any opening in your opponent's program!

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

## Example Challenges

More academic challenges like reversing linked lists or inverting binary trees are fine, if a little boring.

A good challenge is just challenging enough to require some thinking, but easy enough that a complete solution can be written in 15 minutes or less.

Challenges should be accompanied by some sample input and output where possible, but players aren't required to stick to rigid input/output formats unless it's the core feature of the challenge.

For example, if the challenge is reversing a linked list, one player may expect a string of integers separated by arrows to come in from stdin, which they will construct a reversed linked list from - another may expect a pointer to an already constructed linked list, which they should return the reverse of. Both are reasonable and would be accepted.

Challenges that don't have such a well defined input/output structure are welcomed, too. Something like plotting all Starbucks within 50 miles on a map are perfectly acceptible challenges as well.

## Counting Lines

Line counting will change a bit based on the language.
In general, a line is defined as a standalone expression,
or a pair of expressions that would not be separated by
running a code formatter on the source.
Boilerplate to accept input and formatting punctuation are excluded. For example, the following program has 4 lines.
```javascript
function filterOddNumbers(arr){
    let newArr = [];
    for(let elem of arr){
        if(elem % 2 === 0) newArr.push(elem);
    }
    return newArr;
}

console.log([1, 2, 3, 4, 5, 6])
```
Because the one-line if is an intentional syntatic feature of the language, but writing it as follows is counted as 5 lines:

```javascript
function filterOddNumbers(arr){
    let newArr = [];
    for(let elem of arr){
        if(elem % 2 === 0){
            newArr.push(elem);
        }  
    }
    return newArr;
}

console.log([1, 2, 3, 4, 5, 6])
```

And the following is 7 lines:
```javascript
function filterOddNumbers(arr){
    let newArr = [];
    for(let elem of arr){
        if(elem % 2 === 0){newArr.push(elem);} else {something()}  
    }
    return newArr;
}

console.log([1, 2, 3, 4, 5, 6])
```

Because that if/else block would be divided into multiple
lines having had a code formatter run on it.


The following has one line.

```javascript
function filterOddNumbers(arr){
    return arr.filter(elem => elem % 2 === 0)
}
console.log([1, 2, 3, 4, 5, 6])
```

Different things will fly in different languages. When in doubt, leave it up to the opinion of the table, or if you're all super competative, put all code through the same formatter and count every line with no exceptions.