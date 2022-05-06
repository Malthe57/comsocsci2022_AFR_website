---
title: Home Page
layout: single
next: data-description
---

# Amazon reviews

Amazon is the largest online retailer in the world. This means that they offer a large variety of products, across many categories, such as books, electronics and even food.

Because there are so many products available on Amazon, a consumer needs a few metrics they can use to decide whether or not to buy something. 
Amazon has both ratings (from 1 to 5, 1 being lowest) and text reviews, given by other comsumers. 
If a cumstomer decides not to buy a given product, they can always look at some of the many "related products" that are recommended on each products page.

To better understand the ratings and recommendations of Amazon, we looked into how the "related products" recommendations work as a network as well as the behavior of reviwers on the site. 
We did this by looking at data of food products with the "Gourmet food and grocery" tag.

## [Data](data-description)
We used some data! Here it is.


[Click here](data-description) for a more in depth description of the ***data*** we used




## [Network Analysis](network-analysis)
We did some network analysis. We made two networks from the data using the networkx package and looked at community modality.
We also made Louvain communities and compared them with the category-communities.

![](/images/358notags.png)


[Click here](network-analysis) to see what we did and how we did it.



## [Text Analysis](text-analysis)
We did some text analysis on some review text. We also made word clouds and looked at how happiness scores for the reviews matches up with the ratings.

[Click here](text-analysis) to see what we did and how we did it.

## Code chunk

```
import pandas as pd

df = pd.DataFrame()
```


> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nam nec mauris aliquet, convallis ligula vel, mollis est. Fusce accumsan massa vel lectus dapibus, at vehicula elit auctor.

| Column 1  | Column 2  |  Column 3 |
|---|---|---|
| 1 | 4 | 7 |
| 2 | 5 | 8 |
| 3 | 6 | 9 |

## [Explainer Notebook](explainer-notebook.html)

To see our code and more in-depth explanations for our methods and visualisations you can see the explainer notebook [here](explainer-notebook.html)

