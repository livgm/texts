# Facial recognition and racial bias

The topic of Artificial Intelligence and Facial Recognition is slowly but surely being integrated in all parts of our daily lives - whether it be using Snapchat filters, logging in on an iPhone or the police using facial recognition techniques to identify criminals. All of this seems incredibly handy, but it does not work for everyone. Facial recognition techniques are significantly less likely to correctly identify a Black woman than to identify a white woman. This blog post seeks to explain what the problem is, the reasons behind it and suggest ways to improve this.

## The problem

On May 24th, 2019 Alexandra Ocasio-Cortez questioned Joy Buolamwini, a MIT graduate and founder of the "Algorithmic Justice League", an organization that is challenging racial and gender-based bias in Machine Learning, in a congressional hearing on the effectiveness of facial recognition algorithms.

> <b> Ocasio-Cortez: </b> Ms. Buolamwini, I heard your opening statement and we saw that these algorithms are effective to different degrees. So, are they most effective on woman? </br>
<b> Buolamwini: </b> No </br>
<b> Ocasio-Cortez: </b> Are they most effective on people of color? </br>
<b> Buolamwini: </b> Absolutely not. </br>
<b> Ocasio-Cortez: </b> Are they most effective on people of different gender expressions? </br>
<b> Buolamwini: </b> No, in fact, they exclude them. </br>
<b> Ocasio-Cortez: </b> So what demographic are they mostly effective on? </br>
<b> Buolamwini: </b> White men. </br>
<b> Ocasio-Cortez: </b> And who are the primary engineers and designers of these algorithms? </br>
<b> Buolamwini: </b> Definitely white men. </br>


Based on Joy Buolamwini's research for her master's thesis titled <b> Gender Shades </b>, IBM's facial recognition software misgenders Black women almost 35% of the time as compared to 0.3% for white men.

[![statistics.png](https://i.postimg.cc/xdnGLbdZ/statistics.png)](https://postimg.cc/bZV2hrk0)
<sub> Source: [Gender Shades](http://proceedings.mlr.press/v81/buolamwini18a/buolamwini18a.pdf) Page 9.</sub>

If facial recognition is being used in as many situation as it is right now, we have a duty to make sure that it works on everyone and not just on the people who look like most programmers.
## Impact

Facial recognition is used everywhere. Your phone can probably be unlocked by your face, Snapchat can put filters on your face and Google Photos can tag your photos with the names of people it thinks are in the picture. This offers a lot of benefits to people who these pieces of software can recognize easily.

Scandals concerning facial recognition and racial bias have emerged over the years. </br>
In 2015, Google Photos [flagged pictures of Black people as pictures of gorillas](https://www.wired.com/story/when-it-comes-to-gorillas-google-photos-remains-blind/). Google said they were "appalled and genuinely sorry" and blocked the entire label "gorillas".

ProPublica started an investigation into the software used in courtrooms to predict whether or not the person in prison is likely to commit another crime.
>"The formula was particularly likely to falsely flag black defendants as future criminals, wrongly labeling them this way at almost twice the rate as white defendants.
"</br>
<sub>Source: [ProPublica](https://www.propublica.org/article/machine-bias-risk-assessments-in-criminal-sentencing) </sub>

It did not only wrongly label black people as being at higher risk for committing a crime, but also labelled white people with a history of criminality as being less likely to commit another crime than a first-time Black offender. As the topic of mass incarceration in the US is still relevant, this is an important fact to consider.  

After the
## Background information

Facial recognition is a subset of Machine Learning, a branch of Artificial Intelligence. It seeks to detect people's faces, pull information from the expression, depict pictures on to it or store it to use it to later verify people.

A so-called "model" is created by engineers by giving the algorithm a training set, a dataset that is supposed to model the actual values are going to be used later. The model then trains itself by adjusting its parameters used to determine certain pre-determined outputs for the entries of the dataset. </br>
This behaviour mimics the learning process of a human- we learn by recognizing patterns, updating our knowledge and then applying our knowledge to new situations </br>
The dataset that is chosen for training is crucial to the success of the Machine Learning algorithm, as it has to closely mimic the actual test dataset. If all you had ever seen in your life was a car, you certainly could not identify a tree as a tree. This is why it is important to "expose" the model to a dataset that reflects the real world application.

The main demographic in Computer Science is white men, as shown in the [StackOverflow Developer's Survey](https://insights.stackoverflow.com/survey/2019/#demographics). StackOverflow is a heavily used platform for programmers all over the planet to ask questions about programming. According to their survey conducted in 2019, almost 71% of their respondents were white and 90% of all respondents were men. This gender and race disparity has existed in Computer Science for a long time. The first "computers" were women of color computing  complex equations for NASA and similar institutions but since then the primary demographics in the start-up scene and today's Computer Science world has shifted.
https://www.nytimes.com/2016/06/26/opinion/sunday/artificial-intelligences-white-guy-problem.html

## Explanation

Artifical Intelligence by itself has no moral compass, values or bias. It simply inherits and amplifies our own bias.
