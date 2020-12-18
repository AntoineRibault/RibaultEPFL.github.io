---
layout: page
cover-img: /img/bg.jpg
title : Fraises TagADA
subtitle: Assessing Racial Bias Relative to Political Partizanship
---

# Introduction

Racial bias in police decision is at the center of many discussions throughout the world. In particular in the United-States of America, we saw during the 2020 summer the rise of the black lives matter movement that followed the murder of Georges Floyd by police officers. In this context, it seems necessary from a social point of view to understand if a racial bias really exists, and if so, understand it's source.

The <a href="https://openpolicing.stanford.edu">Open Policing Project</a> conducted by a group of researchers at Stanford University assessed the presence or not of a racial bias in police stops in the USA. Using serveral tests, they found that black drivers and hispanic drivers were consistently more stopped and searched than white drivers, suggesting a racial bias in police stop decision.

However, They did not seek for an explanation of such a racial bias. In our extension to their work, we explored the possibility that the policital partizanship of a state could influence the observed racial bias in police stop decisions.

# The Datas

In order to conduct such an exploration, we decided to focus on 6 states (3 democratic and 3 republicans) whose political partizanship is well established and stable over time. Those 6 states include: Texas (Republican), Arizona (Republican), South Carolina (Republican), California (democrat), Illinois (Democrat) & Connecticut (Democrat). We also decided, for a first analysis, to focus on a 3 years window (from 2013 to 2015), to have a preliminary idea of potential differences between the two groups: republican states and democrat states. In order to simplify our analysis, we excluded all the other possible political groups.

The selected states and their affiliated partisanship are summarized in the following map :

{% include state.html %}

# Incidence in police stops, a first approach

To get a first idea of differences in police stops across states, it could be interesting to look at the stop incidence per 100 inhabitants in the 6 concerned states. The incidence is shown on the second map (Map.2).

{% include incidence.html %}

Of course, stops incidence has been calculated taking into account that every race (black, hispanic, or white) is not equally represented in the state.
It is already possible to see that, in function of one's race, disparities in police stops arise. For e.g, in California, a black driver (incidence: 27.86) has more chance to be stopped than an hispanic driver (18.62), or a white driver (25.14). In the contrary, in Texas, a white driver has more chance to be stopped relatively to white people in the state, compared to black or hispanic drivers.
Thus, we can already see that there are disparities in police stops across states.

# La suite

mean search rates:

{% include Mean_search_rates_2013-2015.html %}

relative difference:


exemple 1:

{% include Biases_2013-2015_barplot.html %}

exemple 2:

{% include Biases_2013-2015_slider.html %}

# Threshold test: confirmation of our observation?
Comparing search rates indicate that minorities tend to be searched more often than white individuals. When looking at it like this, people hastily assume discrimination. However, this comparison suffers from the problem of infra marginality : minorities could be searched more because they are more often in possession of contraband. To answer this question, the Threshold test comes into play. The threshold test combines information on search rates and hit rates (the rate at which contraband is actually found). The threshold values indicates the standard of evidence officers require before carrying out a search. The next plot shows the threshold value of black or hispanic over the threshold value of white. If the search rate is justified by the hit rate for all ethnicities, then the threshold values should be similar, and therefore be close to the identity line.

In order to confirm our observations, we applied the threshold test used in the <a href="https://openpolicing.stanford.edu">Open Policing Project</a> to confirm a potential bias in police stops.
Briefly, the idea of the threshold test is that if the bar for searching an individual is lower for a certain race, then, there is a possibility that there is a racial bias against that race. As shown in their work, the Stanford University team demonstrated with the threshold test that there were a racial bias against black drivers, showing that the bar for searching black drivers is lower than for searching white drivers. What could interest us here is to know if there is a correlation between political partizanship and the driver's race.

{% include thresh_white_black.html %}

# Racial Bias evolution over time

Over the last decades, descriminated ethnicities have fought for equality through manifestations and other means. If the states have taken their voices into account then changes in disparities could be observed through time. Therefore, the next plot will be about search rates over time.

{% include searchrate_over_time.html %}

Now lets see the evolution of relative search rates overtime:

{% include bias_over_time.html %}

# KMeans

KMEANS !!!
{% include KMeans.html %}

## nino
