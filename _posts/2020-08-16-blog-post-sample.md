---
title: 'A Chance of Rain'
date: 2020-08-16
permalink: /posts/2020/08/a-chance-of-rain/
tags:
---

I was always confused by what a "chance of rain" meant (before I started graduate school and worked on probabilistic forecasts). It's an odd way to represent a prediction - in practice, people just want to know whether or not it will rain. A "chance of rain" doesn't give me any information on whether to postpone my outdoor plans other than to keep an eye on my weather app. Despite this, people still have a general sense of probability. For instance, a 10% chance of rain means you can probably go on that run, but a 90% chance of rain means you probably don't need to water your garden.

If it isn't obvious, probabilistic forecasts are a way to represent uncertainty in a forecast. Sometimes, this uncertainty is so large we can only predict a 50% chance of rain (which is often the case for thunderstorms), while other times, we are so certain it will rain (for instance, with a hurricane) that we can issue a 100% chance of rain forecast. I'll discuss how we determine this uncertainty in a future post.

Two of the most common metrics (among many) to calibrate probabilistic forecasts are (1) reliability, and (2) sharpness.

### Reliability
The property of a probabilistic forecast is reliability, which we'll understand through an analogy. If a reliable friend told you "I'll be by your house at 3 pm", you would believe that he/she would follow up on that promise. Furthermore, it would be easy to check on whether or not the promise was fulfilled - just check if your friend is at your house by 3 pm. Now, what if your friend told you, "There's a 50% chance I'll be at your house by 3 pm". How would you evaluate the accuracy of this statement? Well, one way would be to track all of the times this person made this statement, and then tally the number of times that this person followed through on this promise. The "50% chance" statement would be accurate if the person was at your house by 3 pm, 5 out of 10 times that he/she made that statement.

This, in essence, is what a 50% chance of rain means: 5 out of 10 times a 50% chance of rain forecast is made, it will rain.
However, a note of caution is that this is only a property of a **reliable** forecast. After all, you wouldn't
trust that one flaky friend after the 100th statement of "I'll be there by 3 pm" turns out to be false, to no one's surprise.

*Side note: wouldn't it be interesting if people made promises based on a percent chance?*

### Sharpness
The second property is called sharpness, and has to do with the frequency of probabilities on the extreme spectrum (i.e. 0% or 100%). If, every single day, your local meteorologist said there was a 50% chance of rain, eventually, you would stop tuning into the forecast because the information becomes useless (note, if you lived in an (extremely rainy) area where it rained every other day, this kind of forecast would actually be reliable). But, as I alluded to earlier, a forecast of 0% or 100% chance of rain gives you so much more information to go about your day. In other words, we value forecasts of 0% or 100% rain much more than say, forecasts of 50% chance of rain.

There is no such thing as free lunch, however! In practice, 0% or 100% forecasts are much harder to get right - the same way that we often say "I'll *probably* get that done by tomorrow", as opposed to "I'll *definitely* get that done by tomorrow". So, the degree of sharpness of a probabilistic forecast measures how many 0% or 100% forecasts there are compared to forecasts of percentages in the middling range, around 40%-60% (this isn't *exactly* right but we'll explore this further in another post).

In summary, both reliability and sharpness are required for a "good" probabilistic forecast. We want forecasts that we can rely on - if there is forecast that says it won't rain, it *better* not rain. At the same time, we want forecasts with certainty as much as possible - a forecast of 50% chance of rain everyday does us no good. As such, forecasts strive to make as many 0% or 100% probability forecasts as possible, but that is not always practical!