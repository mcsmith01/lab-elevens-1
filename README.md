# Elevens Lab

This repository contains all of the code required to complete the portions of the Elevens lab that we will be doing in this class. I have reproduced any questions from the lab here; you should answer them in this document. Remember to commit and push your code once you have completed each portion of the lab.

## Elevens 2 Questions
1. Explain in your own words the difference between a deck and a card.

2. Consider the deck initialized with the statements below. How many cards does the deck contain?
```java
String[] ranks = {"jack", "queen", "king"};
String[] suits = {"blue", "red"};
int pointValues = {11, 12, 13};
Deck d = new Deck(ranks, suits, pointValues);
```

3. The game of Twenty-One is played with a deck of 52 cards. Ranks run from Ace (highest) down to 2 (lowest). Suits are spades, hearts, diamonds, and clubs as in many other games. A face card has a point value of 10; an Ace has a point value of 11; point values for 2...10 are 2...10, respectively. Specify the contents of `ranks`, `suits`, and `pointValues` so that the statement
```java
Deck d = new Deck(ranks, suits, pointValues);
```
initializes a deck for a Twenty-One game.

4. Does the order of elements of the `ranks`, `suits`, and `pointValues` arrays matter?

## Elevens 3 Questions
1. Write a static method named `flip` that simulates a flip of a weighted coin by returning "`heads`" or "`tails`" each time it is called. The coin is twice as likely to turn up heads as tails. Thus, `flip` should return "`heads`" twice as often as it turns up "`tails`."

2. Write a static method `arePermutations` that, given two `int` arrays of the same length but with no duplicate elements, returns `true` if one array is a permutation of the other (i.e., the arrays differ only in how their contents are arranged). Otherwise, it should return `false`.

3. Suppose that the initial contents of the `values` array in `Shuffler.java` are `{1, 2, 3, 4}`. For what sequence of random integers would the efficient selection shuffle change values to `{4, 3, 2, 1}`?

## Elevens 6 questions
1. List all possible plays for the board 5♠ 4♥ 2♦ 6♣ A♠ J♥ K♦ 5♣ 2♠

2. If the deck is empty and the board has three cards left, must they be J, Q, and K? Why or why not?

3. Does the game involve any strategy? That is, when more than one play is possible, does it matter which one is chosen? Briefly explain your answer.

## Elevens 7 questions
1. What items would be necessary if you were playing a game of Elevens at your desk (not on the computer)? List the private instance variables needed for the `ElevensBoard` class.

2. Write an algorithm that describes the actions necessary to play the Elevens game.

3. Now examine the partially implemented `ElevensBoard.java` file found in this repository. Does the `ElevensBoard` class contain all the state and behavior necessary to play the game?

4. `ElevensBoard.java` contains three helper methods. These helper methods are private because they are only called from the ElevensBoard class.
a. Where is the `dealMyCards` method called in ElevensBoard?

b. Which `public` methods should call the `containsPairSum11` and `containsJQK` methods?

c. It’s important to understand how the `cardIndexes` method works, and how the list that it returns is used. Suppose that `cards` contains the elements shown below. Trace the execution of the `cardIndexes` method to determine what list will be returned. Complete the diagram below by filling in the elements of the returned list, and by showing how those values index `cards`. Note that the returned list may have less than 9 elements.

`cards`

| 0  | 1  |  2   | 3  |  4   |  5   | 6  | 7  |  8   |
|----|----|------|----|------|------|----|----|------|
| J♥ | 6♣ |`null`| 2♠ |`null`|`null`| A♠ | 4♥ |`null`|

`returned list`

| 0  | 1  | 2  | 3  | 4  | 5  | 6  | 7  | 8  |
|----|----|----|----|----|----|----|----|----|
|    |    |    |    |    |    |    |    |    |

d. Complete the following `printCards` method to print all of the elements of cards that are indexed by `cIndexes`.
```java
public static printCards(ElevensBoard board) {
	List<Integer> cIndexes = board.cardIndexes();
	/* Your code goes here. */
```

e. Which one of the methods that you identified in question 4b above needs to call the `cardIndexes` method before calling the `containsPairSum11` and `containsJQK` methods? Why?
