---
layout: post
title: Propositions, Logical Operators, and Truth Tables | Study Notes
permalink: /propositions/
date: 2020-08-02
mathjax: true
---

* [Syllabus](/studynotes)
* Prerequisites: None
* Further readings: [Conditional statements](/conditionals), [Propositional Equivalences](/equivalences), Digital Logic Design

# Concept 1.1.1

Mathematics is the study of truths. Every mathematical claim can be defined precisely as a combination of smaller truths, or propositions, using logical operators. 

## Propositions

***Definition.*** A proposition is a statement that is either true or false, but not both. 

The following are some true propositions: 

1. Humans are animals. 
2. $1 + 1 = 2$
3. 4 is divisible by 2. 
4. 17 is a natural number. 
5. There does not exist positive integers $a, b, c$ and integer $n > 2$ such that $a^n + b^n = c^n$. 

And some false propositions: 

1. The capital of the United States is Alabama. 
2. $1 + 1 = 3$
3. 4 is divisible by 3. 
4. 12.5 is an integer. 
5. All real numbers in between 0 and 10 are in between -5 and 5. 

The following sentences are not propositions. The first expresses an ambiguous truth. The second is only true under certain circumstances. The third is not a statement of fact. These sentences have their place in literature, algebra, or daily conversations, but not in propositional logic. 

1. Dandelions are the most beautiful flowers. 
2. $x + 2 = 5$
3. Is it raining today?

## Logical Operators

We can construct more complex propositions by modifying and combining propositions with logical operators. 

***Definition*** For a proposition P, the *negation of P* denoted by $\neg P$ and read as "not P", is the statement: "it is not the case that P." 

We can see that the truth values of $\neg P$ will always be opposite to that of $P$. When P is true, $\neg P$ is false; when P is false, $\neg P$ is true. This relation can be expressed in the form of a truth table. Be careful that "it is not the case that P" is not the same claim as "P is false."

| P | $\neg P$ |
|---|----------|
| T | F        |
| F | T        |

<sup>Truth table of negation.</sup>

The following statements are negations of propositions from above: 

1. "It is not the case that humans are animals", or "humans are not animals."
2. "It is not the case that $1 + 1 = 2$", or "$1 + 1 \neq 2$"
3. "It is not the case that the capital of United States is Alabama", or "the capital of United States is not Alabama."
4. "It is not the case that 4 is divisible by 3", or "4 is not divisible by 3."

Other logical operators describe the relation between two propositions. 

***Definition.*** For propositions P and Q, the *conjunction of P and Q* denoted by $P \wedge Q$ and read as "P and Q" is the proposition that "P and Q are both true."

***Definition.*** For propositions P and Q, the *disjunction of P and Q* denoted by $P \vee Q$ and read as "P or Q" is the proposition that "either P or Q are true."

Note that disjunction referrs to an inclusive or. For instance, you may put pork (inclusively) or tomatoes in your burrito bowl. In natural language, however, "or" is sometimes used to denote exclusive or. In a fancy dining restaurant, for example, you may only have either soup (exclusively) or salad for appetizers but not both. 

***Definition.*** For propositions P and Q, the *exclusive disjunction of P and Q* denoted by $P \oplus Q$ and read as "P aut Q" or "P ex-or Q" is the proposition that "either P or Q are true but not both."

Since P and Q can both be true or false, there are $2 \times 2 = 4$ total possibilities, expressed in this truth table. 

| P | Q | $P \wedge Q$ | $P \vee Q$ | $P \oplus Q$ |
|---|---|--------------|------------|--------------|
| T | T | T            | T          | F            |
| T | F | F            | T          | T            |
| F | T | F            | T          | T            |
| F | F | F            | F          | F            |

<sup>Truth table of conjunction, disjunction, and exclusive disjunction.</sup>

A good way to visualize these operators is to use venn diagrams.

![](/Media/propositions-venndiagram.jpeg)
<sup>Venn diagram represenation of logical operators.</sup>

If the symbols are too hard to memorize, consider an empty cup. If it is held upright, then it can store a lot of water. If it is held upside down, and put into a large tub of water, only a small amount of water will get into the cup. The symbol used for exclusive or is simpler to memorize: it's X and O written on top of each other and rotated. 

![](/Media/propositions-symbol.jpeg)
<sup>Visual mnemonics for operator symbols.</sup>

## Application 

Propositionional logic is used to design logic circuits for computers. Suppose that a warning light should turn on only when a parity bit is off and the stored value of a register is either 0 or 1. To express this state in terms of propotions, let P, Q, R respectively stand for: "parity bit is on", "stored value is 0", and "stored value is 1". Then, the warning light should turn on when "not P and (Q or R)", written formally as $\neg P \wedge (P \vee Q)$. 

In logic design, the symbols for logical operators are often simplified. Negation is denoted with an overline, like $\overline{P}$, disjunction as a plus sign, like $P + Q$, and conjunction abbreviated altogether, like $PQ$. So, $\neg P \wedge (Q \vee R)$ can be simplified as $\overline{P}(Q+R)$. 

For intuition of why disjunction and conjunction are treated as if they're addition and multiplication in algebra, consider p and q, positive real numbers smaller than 1. Then, $p + q$ will be larger than $pq$, much like how the area shaded under $P + Q$ in a venn diagram is larger than $PQ$.

In computing, 1 denotes true, and 0 denotes false. Thus, the truth table looks like this. 

| P | Q | R | $\overline{P}$ | $Q+R$ | $\overline{P}(Q+R)$ |
|---|---|---|----------------|-------|---------------------|
| 1 | 1 | 1 | 0              | 1     | 0                   |
| 1 | 1 | 0 | 0              | 1     | 0                   |
| 1 | 0 | 1 | 0              | 1     | 0                   |
| 1 | 0 | 0 | 0              | 0     | 0                   |
| 0 | 1 | 1 | 1              | 1     | 1                   |
| 0 | 1 | 0 | 1              | 1     | 1                   |
| 0 | 0 | 1 | 1              | 1     | 1                   |
| 0 | 0 | 0 | 1              | 0     | 0                   |
<sup>Truth table of the warning light in logic design syntax.</sup>

This truth table can then be used to design a logic circuit that looks like this. 

![](/Media/propositions-logicgate.jpeg)
<sup>Logic circuit for the warning light.</sup>

# Exercises

1. State which of the following are propositions:
    1. It's a nice whether today. 
    2. Earth orbits around the Sun. 
    3. 10 is divisible by 2. 
    4. Is $1 + 1  = 2$?
2. State the negation of the following propositions: 
    1. Aristotle lived before Kant. 
    2. $2x + 5y = 36xy$
3. Given propositions $P, Q, R$ state the following situations in terms of $P, Q, R$ and logical operators. 

    P: It is raining today. 
    Q: Max brought an umbrella today. 
    R: Max returned wet today. 
    
    1. Max didn't bring an umbrella today, but didn't return wet. 
    2. It wasn't raining, but Max returned wet from swimming. 
    3. Max is always unlucky. It is either raining today, or Max brought an umbrella today, but not both. 

4. Write proposition R in terms of P, Q, and logical operators. 
    | P | Q | R |
    |---|---|---|
    | T | T | T |
    | T | F | F |
    | F | T | F |
    | F | F | T |
5. A user submitted the following query to a search engine. Define adequate propositions and express the query in terms of propositions and logical operators. 

    `site:jwpedia.com (intext:logic OR intext:math) -intitle:philosophy`