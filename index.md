---
layout: page
cover-img: /img/bg.jpg
title : Fraises TagADA
subtitle: Assessing Racial Bias Relative to Political Partizanship
---

# Introduction

Racial bias in police decision is at the center of many discussions throughout the world. In particular in the United-States of America, we saw during the 2020 summer the rise of the black lives matter movement that followed the murder of Georges Floyd by police officers. In this context, it seems necessary from a social point of view to understand if a racial bias really exists, and if so, understand it's source.

The <a href="https://openpolicing.stanford.edu">Open Policing Project</a> conducted by a group of researchers at Stanford University assessed the presence or not of a racial bias in police stops in the USA. Using serveral tests, they found that black drivers and hispanic drivers were consistently more stopped and searched than white drivers, suggesting a racial bias in polie stop decision.

However, They did not seek for an explanation of such a racial bias. In our extension to their work, we explored the possibility that the policital partizanship of a state could influence the observed racial bias in police stop decisions.

# The Datas

In order to conduct such an exploration, we decided to focus on 6 states (3 democratic and 3 republicans) whose political partizanship is well established and are not subjected to changes for long period of times. Those 6 states include: Texas (Republican), Arizona (Republican), South Carolina (Republican), California (democrat), Illinois (Democrat) & Connecticut (Democrat). We also decided, for a first analysis, to focus on a 3 years window (from 2013 to 2015), to have a preliminary idea of potential differences between the two groups: republican states and democrat states. In order to simplify our analysis, we excluded all the other possible political groups.

The policial partizanship can be seen on the following map:

{% include state.html %}

# Incidence in police stops, a first approach

To get a first idea of differences in police stops across states, it could be interesting to look at the stop incidence per 100 inhabitants in the 6 concerned states. The incidence is shown on the second map (Map.2).

{% include incidence.html %}

Of course, stops incidence has been calculated taking into account that every race (black, hispanic, or white) is not equally represented in the state.
It is already possible to see that, in function of one's race, disparities in police stops arise. For e.g, in California, a black driver (incidence: 27.86) has more chance to be stopped than an hispanic driver (18.62), or a white driver (25.14). In the contrary, in Texas, a white driver has more chance to be stopped relatively to white people in the state, compared to black or hispanic drivers.
Thus, we can already see that there are disparities in police stops across states.

# La suite

# Threshold test: confirmation of our observation?

In order to confirm our observations, we applied the threshold test used in the <a href="https://openpolicing.stanford.edu">Open Policing Project</a> to confirm a potential bias in police stops.
Briefly, the idea of the threshold test is that if the bar for searching an individual is lower for a certain race, then, there is a possibility that there is a racial bias against that race. As shown in their work, the Stanford University team demonstrated with the threshold test that there were a racial bias against black drivers, showing that the bar for searching black drivers is lower than for searching white drivers. What could interest us here is to know if there is a correlation between political partizanship and the driver's race.

{% include thresh_white_black.html %}
