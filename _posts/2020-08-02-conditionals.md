---
layout: post
title: Conditionals and Logical Equivalence | Study Notes
permalink: /conditionals/
date: 2020-08-02
mathjax: true
---

* [Syllabus](/studynotes)
* Prerequisites: [Propositions, Logical Operators, and Truth Tables](/propositions)
* Further readings: [Propositional Equivalences](/equivalences)

# Concept 1.1.2

Conditional and biconditional connectives, and logical equivalences are similar but different ways to relate two propositions. A conditional is the proposition that if the hypothesis is true, then that the conclusion is true. Biconditional is the hypothesis that the truth values of two propositions are the same. Logical equivalence holds when said hypothesis is true. 

# Conditional Connectives

***Definition.*** For propositions *P* (hypothesis) and *Q* (conclusion), the *conditional statement* $P \rightarrow Q$ is the proposition "if P, then Q." It is false when *P* is true and *Q* is false, and true otherwise.  

| $P$ | $Q$ | $P \rightarrow Q$ |
|-----|-----|-------------------|
| T   | T   | T                 |
| T   | F   | F                 |
| F   | T   | T                 |
| F   | F   | T                 |

<sup>The truth table of a conditional statement.</sup>

Consider the propositions "If $1 + 1 = 2$ then dogs can't fly", and "If dogs can't fly, then the Sun orbits around the Earth." The former is a true statement, and the latter, false. From these examples, we can see that $T \rightarrow T$ is true, and $T \rightarrow F$ is false. 

A trickier concept is the notion that a false hypothesis always results in a true conditional. How does "If dogs can fly, then $1 + 1 = 0$" make any sense? The real answer is that it often doesn't, and that it is a promise made for some nice properties. 

For a more intuitive understanding of why $F \rightarrow F$ is true, consider the statement: "If I get a hundred subscribers, then I will do a giveaway." Suppose that I never reach a hundred subscribers such that the proposition "I have a hundred subscribers" is false, and that I lied about ever intending to do a giveaway. However, my ten subscribers have not given up the expectation that I will do a giveaway in the future. Thus, my ten subscribers have no reason to believe my promise is false. 

The simplest way to remember the truth table for conditional statements is that it is only false when the hypothesis is true, and the conclusion false. 

Given a conditional statement, three other related conditional statements can be formed. 

***Definition.*** Let $P \rightarrow Q$ be a conditional statement. It's *converse* is $Q \rightarrow P$, its *inverse* $\neg P \rightarrow \neg Q$, and its *contrapositive* $\neg Q \rightarrow \neg P$. 

# Biconditional and Logical Equivalence

***Definition.*** Given propositions *P* and *Q*, the *biconditional statement* $P \leftrightarrow Q$ is the statement that "*P* if and only if *Q*." In other words, the biconditional is the statement that *P* and *Q* have the same truth values. 

| $P$ | $Q$ | $P \leftrightarrow Q$ |
|-----|-----|-----------------------|
| T   | T   | T                     |
| T   | F   | F                     |
| F   | T   | F                     |
| F   | F   | T                     |

<sup>The truth table for a biconditional statement.</sup>

Knowing the definition of a biconditional gives us an ability to make logical arguments. 

***Definition.*** A proposition is a *tautology* if it is always true, and a *contradiction* if it is always false. A proposition is *satisfiable* if it is not a contradiction. 

This is the first occurance of a meta-logical statement. The proposition that "*P* is a tautology" may or may not be true, depending on the truth values of P. For instance, the proposition "$1+1=0$ is a tautology" is false. Then, how are we ever to know whether to trust someone's assertion that a proposition is a tautology (or a contradiction)? 

We introduce - but not elaborate on - the concept of meta-logic, a higher form of logic that governs propositional logic. If I make the metalogical statement that *P* is a tautology, then you can trust me all the time. On the other hand, if I make the proposition that "*P* is a tautology", *P* may not actually be a tautology. 

***Definition.*** Propositions *P* and *Q* are *logically equivalent* such that $P \Leftrightarrow Q$, when the biconditional $P \leftrightarrow Q$ is a tautology. 


$P \Leftrightarrow Q$ is a metalogical statement that the truth values of P and Q are always the same. In the world of propositional logic, we need equivalence in the definition of equivalence itself, like so: $(P \Leftrightarrow Q) \Leftrightarrow ((P \leftrightarrow Q) \Leftrightarrow T)$. This is because the definition of logical equivalence is that the biconditional is logically equivalent to *T*. While this recursive definition is usually adequate, metalanguages may be used to avoid conflicts. Metalanguages are outside the scope of this article, and knowing that it exists will suffice for now. 

*Note.* Biconditional is logically equivalent to $P \rightarrow Q \wedge Q \rightarrow P$. This is precisely why $F \implies P$ is always true. Showing why is left as an exercise. 

Logical equivalences can be shown through truth tables, or by using known logical equivalences. 

***Example 1.*** Show that the following theorem is true: Conjunction is commutative such that for propositions *P* and *Q*, $P \wedge Q \Leftrightarrow Q \wedge P$

| P | Q | $P \wedge Q$ | $Q \wedge P$ |
|---|---|--------------|--------------|
| T | T | T            | T            |
| T | F | F            | F            |
| F | T | F            | F            |
| F | F | F            | F            |

<sup>The truth table for conjunction in both directions.</sup>

Since the truth values of $P \wedge Q$ and $Q \wedge P$ are the same as shown by the truth table, the biconditional $P \wedge Q \leftrightarrow Q \wedge P$ is a tautology. Therefore, $P \wedge Q$ and $Q \wedge P$ are logically equivalent. The commutative property of conjunction is thus shown. 

***Example 2.*** Using the commutative and associative properties (proof is left as an exercise) of conjunction, show that $P \wedge (R \wedge Q)$ is logically equivalent with $P \wedge Q \wedge R$. 

By the commutative property, $P \wedge (R \wedge Q)$ is equivalent to $P \wedge (Q \wedge R)$. Then by the associative property, it is equivalent to $P \wedge Q \wedge R$. 

# Exercises

Since showing logical equivalences is tedious and unnessary, many important logical equivalences are left as optional exercises. It is highly recommended to convince yourself of bolded properties. 

1. Convert each of the following conditional statements into their converse, inverse, and contrapositive, respectively. Then, state the truth values of both. 

    1. If 27 is divisible by 3, then 25 is divisible by 3. 
    2. If $1 + 1 = 2$, then 101 is an odd number. 
    3. If 1.4 is an integer, then 4 is a prime number. 

2. Using a truth table, show that **a conditional statement and its contrapositive are logically equivalent.** 

3. Which of the following are propositions, and which are metalogical statements?
    
    1. $1 + 1 = 2$
    2. $1 + 1 = 2$ is a tautology. 
    3. "$1 + 1 = 2$ is a contradiction."
    4. *P* and *Q* are logically equivalent. 
    5. "It holds that $P \Leftrightarrow Q$"
    
4. Using a truth table, show that the **commutative and associative properties** hold for conjunction and disjunction. 

5. The **De Morgan's Laws** state that 

    $$\neg (P \wedge Q) \Leftrightarrow \neg P \vee \neg Q$$
    
    $$\neg (P \vee Q) \Leftrightarrow \neg P \wedge \neg Q$$
    
    The easiest way to understand the De Morgan's Laws is through a Venn diagram. Convince yourself that the shaded areas are equal to the right side of the above equations. 
    
    ![](/Media/conditionals-demorgans.jpeg)
    <sup>Venn diagram representation of De Morgan's Laws</sup>

    Show the De Morgan's Laws using a truth table. 

6. Using a truth table, show that $P \rightarrow Q \Leftrightarrow \neg P \vee Q$

7. Using a truth table, show that the **absorption laws** hold: 

    $$P \vee ( P \wedge Q ) \Leftrightarrow P$$
    
    $$P \wedge ( P \vee Q ) \Leftrightarrow P$$ 

8. Suppose that the conditional connective $F \rightarrow P$ is always false. Knowing that $P \leftrigharrow Q$ is equivalent to $P \righarrow Q \wedge Q \rightarrow P$, fill out the truth table to show that $Q \leftrightarrow p$ is a contradiction. Why would this be a problem? How does $F \rightarrow P$ being always true solve this issue?











