# Final Project
### Cameron Bale, Neil Duzett, Ryan Gardner

#### What is our problem?
Every year during March Madness, millions of brackets are filled out and submitted with the hope of correctly predicting the outcome of tournament games. The American Gaming Association estimated that 70 million brackets would be filled out to total $10.4 billion overall in bets in 2017.<sup>1</sup> However, no one has predicted all the games in the tournament perfectly. This is a perfect problem to attempt to solve with machine learning, and it has been done before by Alex Tran and Adam Ginzberg at Stanford University in 2014.<sup>2</sup> Our goal will be to create a machine learning algorithm that, at a minimum, performs better than the best bracket submitted by a human, and hopefully will predict the entire tournament correctly.

#### What data will we use?
Following the example of Alex Tran and Adam Ginzberg, we will scrape ESPN for the tournament game data for the last few years of March Madness and for specific features related to each team in the tournament.

#### How will we solve the problem?
Our approach will be centered around classification algorithms such as logistic regression. We will need to identify a cost or score function. As an example, Tran and Ginzberg use a score function:

<a href="https://www.codecogs.com/eqnedit.php?latex=Score&space;=&space;\sum&space;y_{i}(10&space;*&space;2^{round_{i}&space;-&space;1})" target="_blank"><img src="https://latex.codecogs.com/gif.latex?Score&space;=&space;\sum&space;y_{i}(10&space;*&space;2^{round_{i}&space;-&space;1})" title="Score = \sum y_{i}(10 * 2^{round_{i} - 1})" /></a>

where <a href="https://www.codecogs.com/eqnedit.php?latex=y_{i}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?y_{i}" title="y_{i}" /></a> is a binary variable equal to 1 if the predicted outcome is correct, and <a href="https://www.codecogs.com/eqnedit.php?latex=round_{i}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?round_{i}" title="round_{i}" /></a> is the tournament round in which the outcome took place.

Using this function weights correct predictions in later rounds higher than correct predictions in earlier rounds, since an incorrect prediction in early rounds can ruin a whole bracket.

We will create an initial model as a baseline, which we will attempt to improve on. We will clean, understand, and provide summary statistics and descriptions of our data. We will perform feature engineering and selection followed by the utilization of a wide variety of classification models (which we will learn about during future lectures). Once we have implemented a wide variety of models, we will take the three or so models that performed the best and perform cross-validation and hyperparameter tuning to hone in on our best model(s). If possible, we will perform boosting or stack our models to attempt to create the best bracket possible.

We plan to attempt to build on the work of Tran and Ginzberg by obtaining more data from additional tournament years and scraping additional team features. Tran and Ginzberg lament the lack of available, detailed data from ESPN as the greaatest flaw in their research. Now, four years later, there are twice as much data available from the same source. We plan to use these new data as well as additional features such as inter-temporal features on coaches and programs. These new data will allow us to use better hyperparameters from higher-fold cross validation, decrease variance, etc. Additionally, we will attempt to implement additional models besides logistic regression and an SVM, which were the primary models used by Tran and Ginzberg.

#### Supporting documents

<sup>1</sup> https://bleacherreport.com/articles/2697846-march-madness-2017-70-million-brackets-104-billion-in-bets-expected

<sup>2</sup> http://cs229.stanford.edu/proj2014/Adam%20Ginzberg,%20Alex%20Tran,%20Making%20Sense%20of%20the%20Mayhem-%20Machine%20Learning%20and%20March%20Madness.pdf
