---
title: Text analysis
prev: network-analysis
---
<!DOCTYPE html>
<html>
<head>
<style>
blockquote p {
    padding:0;
    margin:100;
}
</style>

The most interesting part of this food review network is of course the reviews themselves, as they contain subjective opinions on different products. 
Therefore, the main idea is to use the reviews for sentiment analysis, using the labTM dictionary of happiness scores 😏

The words in the labTM dictionary are rated on a continuous scale from <font color='red'>1 (low happiness)</font> to 
<font color='#2cbf15'>9 (high happiness)</font>, where a happiness score of <font color='orange'>5</font> indicates <font color='orange'>neutral</font>[^1]. 
[^1]: Reagan et al. (2017): <i> Sentiment analysis methods for
understanding large-scale texts: a case for
using continuum-scored words and word
shift graphs </i>

An example of a review with a high happiness score could be:
<img src="/images/products/candy_crate.jpg" alt="picture of candy crate" style="float:right;width:100px">
<br>**Product:** Candy Crate 1960's Retro Candy Gift Box
<br>**Rating:** 5/5
<br>**Review:** 
>Fun candy that made a fun gift for my Dad. It was well put together with novelty candies and he enjoyed the gift. fun candy

Looking at the tokens found in the labTM dictionary, we see they are all on the positive side:
<br>**Overall happiness:** 7.22
<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  overflow:hidden;padding:10px 5px;word-break:normal;}
.tg th{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  font-weight:normal;overflow:hidden;padding:10px 5px;word-break:normal;}
.tg .tg-0pky{border-color:inherit;text-align:left;vertical-align:top}
.tg .tg-0lax{text-align:left;vertical-align:top}
</style>
<table class="tg">
<tbody>
  <tr>
    <td class="tg-0pky"><span style="font-weight:bold">Token</span></td>
    <td class="tg-0pky">fun</td>
    <td class="tg-0pky">candy</td>
    <td class="tg-0pky">made</td>
    <td class="tg-0pky">fun</td>
    <td class="tg-0pky">gift</td>
    <td class="tg-0pky">dad</td>
    <td class="tg-0pky">well</td>
    <td class="tg-0pky">put</td>
    <td class="tg-0pky">together</td>
    <td class="tg-0pky">enjoyed</td>
    <td class="tg-0pky">gift</td>
    <td class="tg-0pky">fun</td>
    <td class="tg-0pky">candy</td>
  </tr>
  <tr>
    <td class="tg-0pky"><span style="font-weight:bold">Happiness</span></td>
    <td class="tg-0pky">7.96</td>
    <td class="tg-0pky">7.52</td>
    <td class="tg-0pky">5.96</td>
    <td class="tg-0pky">7.96</td>
    <td class="tg-0pky">7.72</td>
    <td class="tg-0pky">7.02</td>
    <td class="tg-0pky">6.68</td>
    <td class="tg-0pky">5.04</td>
    <td class="tg-0pky">6.80</td>
    <td class="tg-0pky">8.02</td>
    <td class="tg-0pky">7.72</td>
    <td class="tg-0pky">7.96</td>
    <td class="tg-0pky">7.52</td>
  </tr>
</tbody>
</table>

An example of a review with a low happiness
<img src="/images/products/cheese_balls.jpg" alt="picture of cheese balls" style="float:right;width:100px">
<br>**Product:** Cheese Balls with Real Cheese Snack, 35 Ounce
<br>**Rating:** 1/5
<br>**Review:** 
>Stale as all get out! Do not buy! Learn from my bad! Do not waste your money! Gag! Ack ! Barf! NASTY!!!

The tokens for this review are quite a bit lower.
<br>**Overall happiness:** 4.88
<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  overflow:hidden;padding:10px 5px;word-break:normal;}
.tg th{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  font-weight:normal;overflow:hidden;padding:10px 5px;word-break:normal;}
.tg .tg-0pky{border-color:inherit;text-align:left;vertical-align:top}
.tg .tg-0lax{text-align:left;vertical-align:top}
</style>
<table class="tg">
<tbody>
  <tr>
    <td class="tg-0pky"><span style="font-weight:bold">Token</span></td>
    <td class="tg-0pky">get</td>
    <td class="tg-0pky">buy</td>
    <td class="tg-0pky">learn</td>
    <td class="tg-0pky">bad</td>
    <td class="tg-0pky">waste</td>
    <td class="tg-0pky">money</td>
    <td class="tg-0pky">nasty</td>
  </tr>
  <tr>
    <td class="tg-0pky"><span style="font-weight:bold">Happiness</span></td>
    <td class="tg-0pky">5.92</td>
    <td class="tg-0pky">6.28</td>
    <td class="tg-0pky">6.70</td>
    <td class="tg-0pky">2.64</td>
    <td class="tg-0pky">2.70</td>
    <td class="tg-0pky">7.30</td>
    <td class="tg-0pky">2.62</td>
  </tr>
</tbody>
</table>
Often, however, the sentiment will be positive even though the context is negative, e.g. <i>buy</i> is positive 
even though the context <i>Do not buy!</i> is negative.

This is very clear in this positive review:
<img src="/images/products/dave_sauce.jpg" alt="dave's hot sauce" style="float:right;height:100px">
<br>**Product:** Dave's Original Insanity Hot Sauce - 5oz
<br>**Rating:** 5/5
<br>**Review:** 
>but also very temporaryMega heat, without the lasting burn of other sauces, which means I can consume more in less time. Is very insanity

**Overall happiness:** 4.48
<br>The tokens <i>heat, burn, without, less, insanity</i> are quite negative, giving the low happiness score of 4.48, 
even though the reviewer is satisfied with his product.

For each product, all reviews are concatenated a long list of tokens. Then the happiness scores for each product is calculated.
Using the food subcategories as decribed in the [data section](../data), the figure below shows the happiness score as a function of 
mean rating for each product:
<img src="/images/linear_corr.png" alt="happiness and mean rating">
As seen in the best linear fit on the points in the figure, the correlation is indeed positive. Using Pearson's linear correlation coefficient
$$
r=\frac{\sum\left(x_i-\mu_x\right)\left(y_i-\mu_y\right)}{\sqrt{\sum\left(x_i-\mu_x\right)^{2} \sum\left(y_i-\mu_y\right)^{2}}},
$$
where 
<math><msub><mi>μ</mi><mrow><mi>x</mi></mrow></msub></math> is the mean of vector <math><mi>x</mi></math>, 
and <math><msub><mi>μ</mi><mrow><mi>y</mi></mrow></msub></math> is the mean of vector <math><mi>y</mi></math>, we get
$$ r = 0.196$$
with a <i>p</i>-value of 0.0002, indicating a significant positive correlation on a 95% confidence level[^2], as expected.
The low correlation coefficient, however, indicates that the effect is quite small. This is likely due to the very simple tabular 
method of sentiment analysis of the labTM dictionary, e.g. not understanding the negative connotation of the bigram "not good", 
instead seeing it as two different tokens. If a more sophisticated method for sentiment analysis was used, 
i.e. one that understood the context of such bigrams, the correlation coefficient would most likely be higher.
[^2]: Calculated using [scipy.stats](https://docs.scipy.org/doc/scipy/reference/generated/scipy.stats.pearsonr.html)

Out of curiousity, the following figure shows the linear correlations for each individual subcategory (with more than 1 data point):

<img src="/images/linear_corrs_b.png" alt="happiness and mean rating subcategories">
Most of the correlations are positive, but for some peculiar reason, the happiness scores for baby foods are almost constant. An idea could be that many of the same tokens, 
like "baby, toddler, infant, milk, formula", are used for both negative and positive reviews. The <i>p</i>-value for the 
slightly negative correlation is far from significant, however. 

<font size="+2"><b>Wordclouds</b></font> <br>
Moving on, the term frequencies (TF) and the term frequence-inverse document frequencies (TF-IDF) were calculated for each subcategory 
in the foodreviews. The words with the highest TF-IDF score are displayed in the wordclouds for the 6 biggest food subcategories:

<img src="/images/wordclouds_b.png" alt="wow wee wordcloud" img style="border:3px solid #3A9A6B;">

Of these 6 food categories, <i>Cooking & Baking, Beverages,</i> and <i>Canned</i> are by far the biggest. Looking at e.g. <i>Cooking & Baking</i>, 
it can at first seem peculiar that a word such as <i><b>Stevia</b></i> (which is an natural sugar substitute) has the highest TF-IDF score, but
considering that this token is only present in two other food categories, it makes sense. The same could be said about <i><b>Xylitol</b></i>,
seen in <i>Candy & Chocolate</i>, which is a sugar substitute often used in gum (also only present in two other categories). 
For <i>Snack Foods</i> we see snacks as <i><b>Popcorn, Jerky</b></i>, and a snack company, <i><b>Welch's</b></i>. For <i>baby foods</i>, 
we have <i><b>Formula, Milk</b></i>, and some baby product brands (and so on). 

Sometimes, the tokens can be very specific for individual products/brands. An example could be <i><b>Keurig</b></i> 
as seen in <i>Beverages</i>, which is a coffee-brewing system using the so-called <i><b>K-cups</b></i>. These specific brands are of course partly
due to the contribution from the IDF score, but also a symptom of the low amount of products for each category (which is even more evident for 
the smaller categories left out of the wordclouds). A larger amount of products would manifest itself in broader terms, and less specific brands.

In general, however, these Wordclouds describe the food categories very well, meaning that the TF-IDF scores give a good indicator for the specific
type of product.