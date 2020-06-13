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

## Naive Bayes For Categorical Data
In this session, you will understand Naive Bayes classifier through an example of mushrooms where the aim is to classify a new mushroom into edible or poisonous class. You will also learn that this algorithm uses probability to do such classification. You will follow the steps given below through the course of this session:
* Bayes Theorem 
* Naïve Bayes on Categorical data

### Naive Bayes -With One Feature
Welcome to the second session of ‘Naive Bayes’. In this session, you will implement Naive Bayes on a mushroom dataset. So, let's have a quick glance at the structure of the dataset.

[Mushroom Data Subset](datset/Mushroom-Subset.xlsx)

![title](image/mushroom-dataset.JPG)

Type of mushroom is the target variable here. We will now implement Naïve Bayes on this mushroom dataset and try to classify a new test point into either of the two classes – edible or poisonous. As the name suggests, the Naive Bayes algorithm uses Bayes’ theorem to classify new test points. But, how exactly does it do this? 

![title](image/Bayesformaula.JPG)

Before we look at six variables together, lets consider a simplified sample containing only two columns i.e class label Ci (Type of mushroom) & X1 (which is Cap-shape). Lets apply Bayes theorem to classify this data point.

![title](image/mushroom-dataset1.JPG)

![title](image/applying-bayes.JPG)

The effect of the denominator P(x) is not incorporated while calculating probabilities as it is the same for both the classes and hence, can be ignored without affecting the final outcome.

![title](image/mushroom-probability.JPG)

![title](image/solving-bayes.png)

Since probablity of mushroom being edible given x is convex is higher so we can classify it in edible class.


A well-articulated explanation of Naive Bayes on https://stackoverflow.com/questions/10059594/a-simple-explanation-of-naive-bayes-classification

## Conditional Independence in Naive Bayes
In the previous segment, you understood the basic idea behind the working of Naive Bayes and how it is implemented on categorical data consisting of one feature and one target variable. In this case, the calculations for solving the classification problem are very simple as the probabilities can simply be calculated by counting. In this segment, you will understand how Naive Bayes would work if there are more than one feature in the data set.

Let's now consider another problem statement where we have below 3 columns. Lets try to classify a new input whose cap-shape is 'CONVEX' and Cap-surface is smooth.

![title](image/mushroom-dataset2.JPG)

Then apply Bayes theorem:

![title](image/applying-bayes1.JPG)

Naïve Bayes follows an assumption that the variables are **conditionally independent** given the class i.e. P(X = convex,smooth | C= edible) can be written as P(X=smooth | C=edible)\timesP(X=convex | C=edible). The terms P(X=smooth | C=edible) and P(X=convex | C=edible) is simply calculated by counting the data points. Hence, the name “Naïve” because in most real-world situations the variables are not conditionally independent given the class label but most of the times the algorithm works nonetheless.

![title](image/applying-bayes2.JPG)

![title](image/applying-bayes-values.JPG)

![title](image/applying-bayes-values1.JPG)

![title](image/applying-bayes-classification.JPG)

Again in above cases we are not considering the effect of denominator.