# Naive Bayes

## Introduction: Naive Bayes
Welcome to the module on ‘Naive Bayes’.

In this module, you will learn about another type of supervised classification, i.e. Naive Bayes. Naïve Bayes is a probabilistic classifier which returns the probability of a test point belonging to a class rather than the label of the test point. It is used in text based classification. Example classification of ham vs spam.

In this session, you will learn about the Bayes' Theorem and it's building blocks. You will be learning about conditional probability, joint probability and finally Bayes' theorem.

## Conditional Probability and Its Intuition
![title](image/conditional.JPG)

![title](image/conditional1.JPG)

![title](image/conditional2.JPG)

## Bayes' Theorem
In this section, you will understand Bayes’ Theorem for calculating the conditional probability. The example we will use now is something almost all of us can relate to which is cricket.

While watching cricket matches on TV, you may have seen statistics similar to this: “India wins 70% matches when Tendulkar scores a century.” Sounds like conditional probability? This is a classic example of how conditional probability can be used to estimate the chances of an event taking place, given certain other events that have happened.  

Suppose that India plays 100 matches, out of which it wins 60 and loses 40. Also, Sachin Tendulkar plays these 100 matches, scores a century in 12 of them, and doesn't score a century in the rest 88.

To make things interesting, you also have this additional information: out of the 60 games that India wins, Sachin scores a century in 10, and out of the 40 games that India loses, Sachin scores a century only in two.

Let us look how the two-way contingency matrix will look like for the above case :

![title](image/conditional3.JPG)

Now, can you answer this question: what is the probability that India wins, given that Sachin has scored a century?

![title](image/join-conditional.JPG)

## Bayes' Theorem
Let's derive Bayes' theorem using joint and conditional probability using a two-way contingency table example.

![title](image/BayesTheorem.JPG)

We have learnt some important concepts related to Bayes’ theorem, i.e. conditional probability and joint probability.