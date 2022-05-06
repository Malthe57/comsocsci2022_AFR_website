---
title: Home Page
layout: single
next: data-description
---

# <b>Amazon reviews</b>

Amazon is the largest online retailer in the world. This means that they offer a large variety of products, across many categories, such as books, electronics and even food.

Because there are so many products available on Amazon, a consumer needs some information they can use to decide whether or not to buy something. 
Amazon has both ratings (from 1 to 5, 1 being lowest) and text reviews, given by other comsumers. 
If a cumstomer decides not to buy a given product, they can always look at some of the many "related products" that are recommended on each products page.

To better understand the ratings and recommendations of Amazon, we looked into how the "related products" recommendations work as a network as well as the behavior of reviwers on the site. 
We did this by looking at data of food products with the "Gourmet food and grocery" tag.


## [Data](data-description)
The data on Reviews and products for the "Grocery & Gourmet Foods" section on amazon was collected by researchers from UCSD. We used two datasets, one for the reviews and another for products.

[Click here](data-description) for a more in depth description of the data we used, as well as download links for the datasets.


## [Network Analysis](network-analysis)
One way we have examined the data in, is as a network. We made two networks, one that connects reviewers with other reviewers who reviewed the same product. Another network connects products with its related products.
### Reviewer network
To see who the most prevalent user-reviewers on amazons "Grocery & Gourmet Food" section is, we have made a network from reviewers, connecting them to other reviewers who have reviewed the same product.

![](/images/reviewer_network.png)

We take a look at node degrees to see who is the top reviewer.

### Product network
By creating a network where each product is a node that has edges to its related products, we can see how the products in the "Grocery & Gourmet Food" section connect with each other. 

![](/images/network_cats.png)

We also take a look at how well the products category can explain which other nodes it is connected to, and see how it compares to communities partitioned by the Louvain algorithm.

[Click here](network-analysis) to see how we performed the network analysis and what we found out!



## [Text Analysis](text-analysis)
In this section we dove into the review text, to find out what people say about products of different categories. To visualise it, several words clouds were made, showing the most signifigant words from reviews of that category. For example, here is the word cloud for the category "Snack Foods":

![](/images/snackfoodcloud.png)

We also took a look at whether the happiness of the review text typically matches the rating given in the same review.

[Click here](text-analysis) to see the full text analysis.

## [Explainer Notebook](explainer-notebook.html)

To see our code and more in-depth explanations for our methods and visualisations you can see the explainer notebook [here](explainer-notebook.html)

