---
layout: page
cover-img: /img/bg.jpg
title : Fraises TagADA
subtitle: Effect of political partisanship on racial bias in police stops
---

# Chapter 0 - Introduction

The appearance of social movements such as black live matters demonstrate a great feeling of injustice among US citizens regarding ethnicities. Deadly accidents caused by police forces such as the Georges Floyd case spread fear and hatred among everyone. Similar casualties in the police persist and seems to be aimed at minorities. But proving that these minorities are victim of discrimination remains a hefty challenge legally speaking.<br>
<a href="https://openpolicing.stanford.edu">The Open Policing Project</a> conducted by a group of researchers at Stanford University aims at inspecting racial bias during police stops. They collected and standardized over 200 million records of traffic stop and search data from across the USA. Using state of the art test analysis, their data suggest significant racial disparities and show evidence that racial bias also plays a role.
Be that as it may, proving that police decisions are racially biased is just the first step towards reducing racisms. Finding the source for police behavior may help us further. In their study, Stanford University did not seek an explanation for such bias. As an extension to their work, we are interested to know if the political affiliation of a state could influence racial bias in police search decisions. In this data story, we will guide you through our research, so sit comfortably and enjoy the plots!

# Chapter 1 - The Datas

Politics exert influence over citizens. They generate laws and spread ideas, but unfortunately, they are not as objective as we would hope. The messages they transmit vary from one political party to an other. Let us see together whether they correlate with police search decisions.
In order to conduct such an exploration, we decided to focus on states whose political partisanship are well established and are not subject to changes for long periods of time. The chosen states also have to be available on The Open Policing Project on similar time spawns. For simplicity we only consider the two dominant political parties: democratic and republican. We ended up with 7 candidates : 4 democratic states (California, Illinois, Connecticut & Washington) and 3 republican (Texas, Arizona & South Carolina). We summarized the candidates on the following map for you:

{% include state.html %}

# Chapter 2 - Search rates by political partisanship

For this part of the study, we will focus on the 2013-2015 period.

To get a first idea of differences in police stops across states, it could be interesting to look at the stop incidence per 100 inhabitants. To do so, we excluded the Washington state to keep as much democratic states as republican states for a first analysis. Washington will be used later on (we reserved a final "plot" twist for you dear viewer :)). The incidence can be observed on the following map. Don't hesitate to play with it (you can choose which ethnicity to show using the slider)!

{% include incidence.html %}

Of course, stops incidence has been calculated taking into account that every race (black, hispanic, or white) is not equally represented in the state. Also, not all stops have been included in our datas as many of them were incomplete (had to be removed)... <br>
It is already possible to see that, in function of one's race, disparities in police stops arise. For e.g, in California, a black driver (incidence: 27.86) has more chance to be stopped than an hispanic driver (18.62), or a white driver (25.14). In the contrary, in Texas, a white driver has more chance to be stopped relative to white drivers in the state, compared to black or hispanic drivers. <br>
Thus, we can already see that there are disparities in police stops across states.

Let us define a very important parameter for our analysis. Search rates are defined as the proportion of searched drivers over stopped drivers.
Given this definition, we can now take a look at search rates for every race relative to each political party:

{% include Mean_search_rates_2013-2015.html %}

 Democrats tend to search more than republicans, but we cannot interpret much. So instead of comparing raw search rates, let us compare the relative difference between minority (black or hispanic) search rates and white search rates. We hereby invite you to contemplate the next plot.

{% include Biases_2013-2015_slider.html %}

Aha, so we have a culprit ! So now we see that democrats truly have a bigger gap between black driver searches and white driver searches. We can also see that the political partisanship has no influence on the relative difference of search rates between hispanic and white drivers. Is this enough to presume that democrats discriminate more than republicans ? Well, we wouldn’t be asking this question if it was. But the only way to be truly sure would be to keep on reading …

# Chapter 3 - The Threshold test
Comparing search rates indicate that minorities tend to be searched more often than white individuals. When looking at it like this, people hastily assume discrimination. However, this comparison suffers from the problem of infra-marginality : minorities could be searched more because they are more often in possession of contrabands. To answer this question, the Threshold test comes into play. The threshold test combines information on search rates and hit rates (the rate at which contraband is actually found). The values of a Threshold test indicate the standard of evidence officers require before carrying out a search. The next plot shows the threshold value of black drivers over the threshold value of white drivers. If the search rate is justified by the hit rate, then the threshold values should be similar for both ethnicity, and therefore be close to the identity line. Since the probability of having contrabands can vary from one county to the next, we indicate threshold values for each county.

{% include thresh_white_black.html %}

For hispanics, the threshold comparison lies more or less on the diagonal x=y. We cannot clearly infer any discrimination from the republicans nor the democrats. For the black drivers coming from a democratic state however, we see that the search threshold is generally lower than the search threshold for whites (blue bubbles are mainly under the diagonal). So police require less suspicion to search black drivers coming from democratic states than white drivers. Finally a proof of discrimination ! And we do not observe the same results for black drivers coming from republican states. So far, from the selected states, the data suggests that police officers of democratic states have a higher racial bias against black drivers than police officers coming from a republican state.

# Chapter 3.5 - KMeans Clustering

What could be amazing given inferred thresholds is to manage to predict the county's state political partisanship without any trained model. This would comfort us in the idea that there is a real difference in stop policy among republican and democratic states.<br>
Well guess what? We tried! <br>
We applied a famous machine learning method, Kmean clustering, on our black/white inferred threshold to see if a dumb computer could actually recover the political party.

{% include KMeans.html %}

As can be seen, the computer managed, without any label, to separate with a 75% accuracy counties that come from a republican states, and the one that come from democratic states.
No more words on that, it was just a bonus...

# Chapter 4 - Evolution of search rates over time

Over the last decades, descriminated ethnicities have fought for equality through manifestations and other means. If the states have taken their voices into account then changes in disparities could be observed through time.  <br>

A first analysis we could make would be to look out for the evolution of search rates over time:

{% include searchrate_over_time.html %}

As we can see, the search rates for minorities tend to decrease over time in democratic states, whereas they seem to strangely increase from 2016 in republican states. <br>
We made an in depth analysis of what was happening for the republicans in 2016, and we found out that Arizona is responsible for this strange behavior. We did not find any reason for such a weird evolution. <br>

Even though the search rates give us an interesting information on their evolution over time, we fail to interpret the evolution of racial bias. So for this reason, we went further by looking at the evolution of the relative difference between minorities and white search rates (remember the last part of Chapter 2).

{% include bias_over_time.html %}

As can be seen on the figure, it seems that for both political partisanship, the relative difference between minorities and white search rates decreases. This is a good news for the minorities as this suggests that the racial bias diminishes over time!

# Chapter 5 - Conclusion

To conclude, we showed in a first part that black drivers were more searched in democratic states than in republican states. However, this bias seems to decrease over time in the 2012-2016 time window. So to have an idea of the actual 2020 situation, we should do the analysis in a couple of years when the datas will be available to see if a racial bias is still present, and if so, is it still decreasing?

See you in a couple of years for the end of the story!

![Alt Text](https://media.giphy.com/media/dCB2smaPUGHibtEQXi/giphy.gif)

PS: Fraise means strawberry in french!
