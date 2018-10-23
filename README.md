# Final Project
### Cameron Bale, Neil Duzett, Ryan Gardner

#### What is our problem?
Every year during March Madness, millions of brackets are filled out and submitted with the hope of correctly predicting the outcome of tournament games. The American Gaming Association estimated that 70 million brackets would be filled out to total $10.4 billion overall in bets in 2017.<sup>1</sup> However, no one has predicted all the games in the tournament perfectly. This is a perfect problem to attempt to solve with machine learning, and it has been done before by Alex Tran and Adam Ginzberg at Stanford University in 2014.<sup>2</sup> Our goal will be to create a machine learning algorithm that, at a minimum, performs better than the best bracket submitted by a human, and hopefully will predict the entire tournament correctly.

#### What data will we use?
Following the example of Alex Tran and Adam Ginzberg, we will scrape ESPN for the tournament game data for the last few years of March Madness and for specific features related to each team in the tournament.

#### Outline for how we will solve the problem: preprocessing steps, models, etc.
Our approach will be centered around classification algorithms such as logistic regression. We will need to identify a cost or score function. As an example, Tran and Ginzberg use a score function:

<a href="https://www.codecogs.com/eqnedit.php?latex=Score&space;=&space;10&space;*&space;2^{round&space;-&space;1}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?Score&space;=&space;10&space;*&space;2^{round&space;-&space;1}" title="Score = 10 * 2^{round - 1}" /></a>

Using this function weights correct predictions in later rounds higher than correct predictions in earlier rounds, since an incorrect prediction in early rounds can ruin a whole bracket.

We plan to attempt to build on the work of Tran and Ginzberg by obtaining more data from additional tournament years and scraping additional team features. Tran and Ginzberg state, "Perhaps qualitative features about the players on a specific team or inter-temporal features regarding a coach and a specific program may be useful."


#### Supporting documents citing past research and methods used to solve the problem previously

#### Think deep about the project: is it a meaningful and achievable project for this class?

<sup>1</sup> https://bleacherreport.com/articles/2697846-march-madness-2017-70-million-brackets-104-billion-in-bets-expected

<sup>2</sup> http://cs229.stanford.edu/proj2014/Adam%20Ginzberg,%20Alex%20Tran,%20Making%20Sense%20of%20the%20Mayhem-%20Machine%20Learning%20and%20March%20Madness.pdf
