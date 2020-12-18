---
layout: page
cover-img: /img/bg.jpg
title : Fraises TagADA
subtitle: Assessing Racial Bias Relative to Political Partizanship
---

# Chapter 0 - Introduction

The appearance of social movements such as black live matters demonstrate a great feeling of injustice among US citizens regarding ethnicities. Deadly accidents caused by police forces such as the Georges Floyd case spread fear and hatred among everyone. Similar casualties in the police persist and seems to be aimed at minorities. But proving that these minorities are victim of discrimination remains a hefty challenge legally speaking.<br>
<a href="https://openpolicing.stanford.edu">The Open Policing Project</a> conducted by a group of researchers at Stanford University aims at inspecting racial bias during police stops. They collected and standardized over 200 million records of traffic stop and search data from across the USA. Using state of the art test analysis, their data suggest significant racial disparities and show evidence that racial bias also plays a role.
Be that as it may, proving that police decisions are racially biased is just the first step towards reducing racisms. Finding the source for police behavior may help us further. In their study, Stanford University did not seek an explanation for such bias. As an extension to their work, we are interested to know if the political affiliation of a state could influence racial bias in police search decisions. In this data story, we will guide you through our research, so sit comfortably and enjoy the plots.

# Chapter 1 - The Datas

Politics exert influence over citizens. They generate laws and spread ideas, unfortunately they are not as objective as we would hope. The messages they transmit vary from one political party to an other. Let us see together whether they correlate with police search decisions.
In order to conduct such an exploration, we decided to focus on states whose political partisanship are well established and are not subject to changes for long periods of time. The chosen states also have to be available on The Open Policing Project on similar time spawns. For simplicity we only consider the two dominant political parties which are democratic and republican. We ended up with 7 candidates : 4 democratic (California, Illinois, Connecticut & Washington) and 3 republican (Texas, Arizona & South Carolina). We summarized the candidates on the following map for you.

{% include state.html %}

# Chapter 2 - Search rates by political partisanship

To get a first idea of differences in police stops across states, it could be interesting to look at the stop incidence per 100 inhabitants. To do so, we excluded WA to focus on the 6 other states for a first analysis. Washington will be used later on (we reserved a final "plot" twist for you dear viewer :)). The incidence can be observed on the following map, note that you can choose which ethnicity to show using the slider. Don't hesitate to play with it!:

{% include incidence.html %}

Of course, stops incidence has been calculated taking into account that every race (black, hispanic, or white) is not equally represented in the state. Also, not all stops have been included in our datas as many of them were incomplete (had to be removed)... <br>
It is already possible to see that, in function of one's race, disparities in police stops arise. For e.g, in California, a black driver (incidence: 27.86) has more chance to be stopped than an hispanic driver (18.62), or a white driver (25.14). In the contrary, in Texas, a white driver has more chance to be stopped relatively to white people in the state, compared to black or hispanic drivers.
Thus, we can already see that there are disparities in police stops across states.

{% include Mean_search_rates_2013-2015.html %}

Aha, so we have a culprit ! Democrats tend to search more the minorities than republicans. Of course at this point it is just a joke. It would be misleading to assume that racial disparities changes from one state to the other since the total number of search rates varies too. So instead of comparing raw search rates, let us compare the relative difference between minority (black or hispanic) search rates and white search rates. I hereby invite to contemplate the next plot.

Exemple2
{% include Biases_2013-2015_slider.html %}

So now we see that democrats truly have a bigger gap between minority searches and white searches. Is this enough to presume that democrats discriminate more than republicans ? Well, we wouldn’t be asking this question if it was. But the only way to be truly sure would be to keep on reading …

# Chapter 3 - The Threshold test
Comparing search rates indicate that minorities tend to be searched more often than white individuals. When looking at it like this, people hastily assume discrimination. However, this comparison suffers from the problem of infra-marginality : minorities could be searched more because they are more often in possession of contrabands. To answer this question, the Threshold test comes into play. The threshold test combines information on search rates and hit rates (the rate at which contraband is actually found). The values of a Threshold test indicate the standard of evidence officers require before carrying out a search. The next plot shows the threshold value of black or hispanic over the threshold value of white. If the search rate is justified by the hit rate, then the threshold values should be similar for both ethnicity, and therefore be close to the identity line. Since the probability of having contrabands can vary from one county to the next, we indicate threshold values for each county.

{% include thresh_white_black.html %}

For hispanics, the threshold comparison lies more or less on the diagonal x=y. We cannot clearly infer any discrimination from the republicans nor the democrats. For the black democrats however, we see that the search threshold for blacks is generally lower than the search threshold for whites (blue bubbles are mainly under the diagonal). So police require less suspicion to search black drivers than white drivers. Finally a proof of discrimination ! And we do not observe the same results for black republicans. So far, from the selected states, the data suggest that democrats exert higher disparities between black searches and white searches and only democrats discriminate. But a final topic remains to be discussed, that may convince you otherwise …

# Chapter 4 - Evolution of search rates over time

Over the last decades, descriminated ethnicities have fought for equality through manifestations and other means. If the states have taken their voices into account then changes in disparities could be observed through time. Therefore, the next plot will be about search rates over time.

{% include searchrate_over_time.html %}

Now lets see the evolution of relative search rates overtime:

{% include bias_over_time.html %}

# KMeans

KMEANS !!!
{% include KMeans.html %}
