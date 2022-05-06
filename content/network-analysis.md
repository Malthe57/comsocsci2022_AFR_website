---
title: Network analysis
prev: data-description
next: text-analysis
---

We created and investigated two networks: One for the reviewer and one for the products.


# <b> Reviewer network </b>
The goal is to identify the so-called super users on Amazon; users who especially active and write many reviews on Amazon. 

The review network consists of 14,681 nodes and 4,228,404 edges. Due to the sheer size of the network, it is only possible to visualise a subset. The subset consists of reviewers for 500 unique, randomly sampled products, so the resulting network has a total of 5,773 nodes and 229,767 edges. 
<img src="/images/reviewer_network.png" width="1400" />
From the graph, we have identified some nodes with highest degree (largest nodes) which we can look further into:
<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  overflow:hidden;padding:10px 5px;word-break:normal;}
.tg th{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  font-weight:normal;overflow:hidden;padding:10px 5px;word-break:normal;}
.tg .tg-c3ow{border-color:inherit;text-align:center;vertical-align:top}
.tg .tg-nbj5{background-color:#FFF;border-color:inherit;text-align:center;vertical-align:top}
.tg .tg-7btt{border-color:inherit;font-weight:bold;text-align:center;vertical-align:top}
.tg .tg-i45s{background-color:#F5F5F5;border-color:inherit;text-align:center;vertical-align:middle}
.tg .tg-t1ow{background-color:#F5F5F5;border-color:inherit;text-align:center;vertical-align:top}
.tg .tg-rcip{background-color:#FFF;border-color:inherit;text-align:center;vertical-align:middle}
</style>
<table class="tg">
<caption>Table 1: </caption>
<thead>
  <tr>
    <th class="tg-7btt">Reviewer</th>
    <th class="tg-7btt">Reviewer name</th>
    <th class="tg-7btt">Number of reviews</th>
    <th class="tg-c3ow"><span style="font-weight:bold">Node degree</span></th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-i45s">A1ZH9LWMX5UCFJ</td>
    <td class="tg-i45s">K. Stuckey "kateling"</td>
    <td class="tg-t1ow">82</td>
    <td class="tg-c3ow">3178</td>
  </tr>
  <tr>
    <td class="tg-rcip">AYNAH993VDECT</td>
    <td class="tg-rcip">bsg2004</td>
    <td class="tg-nbj5">75</td>
    <td class="tg-c3ow">3701</td>
  </tr>
  <tr>
    <td class="tg-i45s">A1P2XYD265YE21</td>
    <td class="tg-i45s">Andrea "Readaholic"</td>
    <td class="tg-t1ow">67</td>
    <td class="tg-c3ow">3629</td>
  </tr>
  <tr>
    <td class="tg-c3ow">AAA0TUKS5VBSA</td>
    <td class="tg-c3ow">Nerd Alert</td>
    <td class="tg-c3ow">149</td>
    <td class="tg-c3ow">4012</td>
  </tr>
</tbody>
</table>

The table below shows the reviewers with the top 10 most reviews.
<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  overflow:hidden;padding:10px 5px;word-break:normal;}
.tg th{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  font-weight:normal;overflow:hidden;padding:10px 5px;word-break:normal;}
.tg .tg-9ak0{background-color:#ffffff;border-color:#000000;color:#333333;font-weight:bold;text-align:center;vertical-align:top}
.tg .tg-mums{background-color:#ffffff;border-color:#000000;font-weight:bold;text-align:center;vertical-align:top}
.tg .tg-jbyd{background-color:#ffffff;border-color:#000000;text-align:center;vertical-align:top}
.tg .tg-vhtn{background-color:#ffffff;border-color:#000000;text-align:center;vertical-align:middle}
</style>
<table class="tg">
<thead>
  <tr>
    <th class="tg-9ak0">Reviewer</th>
    <th class="tg-mums">Reviewer name</th>
    <th class="tg-mums">Number of reviews</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-jbyd">A3OXHLG6DIBRW8</td>
    <td class="tg-jbyd">C. Hill "CFH"</td>
    <td class="tg-vhtn">204</td>
  </tr>
  <tr>
    <td class="tg-jbyd">AY12DBB0U420B</td>
    <td class="tg-jbyd">Gary Peterson</td>
    <td class="tg-vhtn">180</td>
  </tr>
  <tr>
    <td class="tg-jbyd">A2XKJ1KX6XUHYP</td>
    <td class="tg-jbyd">NYFB</td>
    <td class="tg-vhtn">177</td>
  </tr>
  <tr>
    <td class="tg-jbyd">A1UQBFCERIP7VJ</td>
    <td class="tg-jbyd">Margaret Picky</td>
    <td class="tg-vhtn">156</td>
  </tr>
  <tr>
    <td class="tg-jbyd">AAA0TUKS5VBSA</td>
    <td class="tg-jbyd">Nerd Alert</td>
    <td class="tg-vhtn">149</td>
  </tr>
  <tr>
    <td class="tg-jbyd">A2MNB77YGJ3CN0</td>
    <td class="tg-jbyd">L. Mountford</td>
    <td class="tg-vhtn">145</td>
  </tr>
  <tr>
    <td class="tg-jbyd">A1Z54EM24Y40LL</td>
    <td class="tg-jbyd">csm</td>
    <td class="tg-vhtn">141</td>
  </tr>
  <tr>
    <td class="tg-jbyd">A25C2M3QF9G7OQ</td>
    <td class="tg-jbyd">Comdet</td>
    <td class="tg-vhtn">140</td>
  </tr>
  <tr>
    <td class="tg-jbyd">A2YKWYC3WQJX5J</td>
    <td class="tg-jbyd">Shannon Lastowski "Queen of Caffeine"</td>
    <td class="tg-vhtn">132</td>
  </tr>
  <tr>
    <td class="tg-jbyd">AKMEY1BSHSDG7</td>
    <td class="tg-jbyd">J. Arena</td>
    <td class="tg-vhtn">127</td>
  </tr>
</tbody>
</table>

It is worth noting that among the identified users with the highest node degree, only one of them (Nerd Alert) is among the users with the top 10 most reviews. However, keep in mind that the network has an edge between two nodes if they have reviewed the same product. This means if a product has been reviewed by many people, then the users who have reviewed that product will have many edges. 


Below we have a table for the four identified reviewers + the top 3 reviewers. For each reviewer, the number of reviews, node degree, and the average number of reviews on the products they have reviewed (average review score) are presented. 
<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  overflow:hidden;padding:10px 5px;word-break:normal;}
.tg th{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  font-weight:normal;overflow:hidden;padding:10px 5px;word-break:normal;}
.tg .tg-mums{background-color:#ffffff;border-color:#000000;font-weight:bold;text-align:center;vertical-align:top}
.tg .tg-vhtn{background-color:#ffffff;border-color:#000000;text-align:center;vertical-align:middle}
.tg .tg-jbyd{background-color:#ffffff;border-color:#000000;text-align:center;vertical-align:top}
</style>
<table class="tg">
<thead>
  <tr>
    <th class="tg-mums">Reviewer</th>
    <th class="tg-mums">Reviewer name</th>
    <th class="tg-mums">Number of reviews</th>
    <th class="tg-mums">Node degree</th>
    <th class="tg-mums">Average review score</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-vhtn">A1ZH9LWMX5UCFJ</td>
    <td class="tg-vhtn">K. Stuckey "kateling"</td>
    <td class="tg-jbyd">82</td>
    <td class="tg-jbyd">3178</td>
    <td class="tg-jbyd">74.3780487804878</td>
  </tr>
  <tr>
    <td class="tg-vhtn">AYNAH993VDECT</td>
    <td class="tg-vhtn">bsg2004</td>
    <td class="tg-jbyd">75</td>
    <td class="tg-jbyd">3701</td>
    <td class="tg-jbyd">183.17333333333335</td>
  </tr>
  <tr>
    <td class="tg-vhtn">A1P2XYD265YE21</td>
    <td class="tg-vhtn">Andrea "Readaholic"</td>
    <td class="tg-jbyd">67</td>
    <td class="tg-jbyd">3629</td>
    <td class="tg-jbyd">165.37313432835822</td>
  </tr>
  <tr>
    <td class="tg-jbyd">AAA0TUKS5VBSA</td>
    <td class="tg-jbyd">Nerd Alert</td>
    <td class="tg-jbyd">149</td>
    <td class="tg-jbyd">4012</td>
    <td class="tg-jbyd">126.63087248322148</td>
  </tr>
  <tr>
    <td class="tg-jbyd">A3OXHLG6DIBRW8</td>
    <td class="tg-jbyd">C. Hill "CFH"</td>
    <td class="tg-jbyd">204</td>
    <td class="tg-jbyd">5155</td>
    <td class="tg-jbyd">74.06862745098039</td>
  </tr>
  <tr>
    <td class="tg-jbyd">AY12DBB0U420B</td>
    <td class="tg-jbyd">Gary Peterson</td>
    <td class="tg-jbyd">180</td>
    <td class="tg-jbyd">2789</td>
    <td class="tg-jbyd">20.13888888888889</td>
  </tr>
  <tr>
    <td class="tg-jbyd">A2XKJ1KX6XUHYP</td>
    <td class="tg-jbyd">NYFB</td>
    <td class="tg-vhtn">177</td>
    <td class="tg-jbyd">2374</td>
    <td class="tg-jbyd">19.073446327683616</td>
  </tr>
</tbody>
</table>

The user with the highest number of reviews and node degree is C. Hill "CFH". However, writing many reviews does not equate to having a high node degree. For instance, the user "Gary Peterson" has written the second most reviews with 180, yet only have a node degree of 2,374. Comparatively, another user, "bsg2004" have only written 75 reviews, but have a much higher node degree of 3,701. Based on the average review score, we see that even though the users "Gary Peterson" and "NYFB" have written many reviews, the products that they review are not commonly reviewed by others. 

In conclusion, the reviewer network can be useful to identify some super users. However, the number of times a product has been reviewed needs to be accounted for, since it has a major impact on the node degree.

## <b> Random network </b>

The reviewer network is an example of a real-world network constructed using real data. We would like to construct a random network that has some of the same properties as the reviewer network, and then compare them. The random network consists of the same number of nodes, and with a probability p=0.0392, an edge is established between two independent nodes. Some summary statistics of the two networks are listed below in the table below.

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  overflow:hidden;padding:10px 5px;word-break:normal;}
.tg th{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  font-weight:normal;overflow:hidden;padding:10px 5px;word-break:normal;}
.tg .tg-9ak0{background-color:#ffffff;border-color:#000000;color:#333333;font-weight:bold;text-align:center;vertical-align:top}
.tg .tg-tgze{background-color:#ffffff;border-color:#000000;font-weight:bold;text-align:left;vertical-align:top}
.tg .tg-mums{background-color:#ffffff;border-color:#000000;font-weight:bold;text-align:center;vertical-align:top}
.tg .tg-jbyd{background-color:#ffffff;border-color:#000000;text-align:center;vertical-align:top}
.tg .tg-vhtn{background-color:#ffffff;border-color:#000000;text-align:center;vertical-align:middle}
</style>
<table class="tg">
<thead>
  <tr>
    <th class="tg-9ak0"></th>
    <th class="tg-mums">Reviewer network</th>
    <th class="tg-mums">Random network</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-jbyd"><span style="font-weight:bold">Nodes</span></td>
    <td class="tg-jbyd">14,681</td>
    <td class="tg-vhtn">14,681</td>
  </tr>
  <tr>
    <td class="tg-jbyd"><span style="font-weight:bold">Edges</span></td>
    <td class="tg-jbyd">4,228,404</td>
    <td class="tg-vhtn">4,229,033</td>
  </tr>
  <tr>
    <td class="tg-jbyd"><span style="font-weight:bold">Min. degree</span></td>
    <td class="tg-jbyd">8</td>
    <td class="tg-vhtn">492</td>
  </tr>
  <tr>
    <td class="tg-jbyd"><span style="font-weight:bold">Max. degree</span></td>
    <td class="tg-jbyd">5155</td>
    <td class="tg-vhtn">673</td>
  </tr>
  <tr>
    <td class="tg-tgze">Mean degree</td>
    <td class="tg-jbyd">576.038</td>
    <td class="tg-jbyd">576.12</td>
  </tr>
  <tr>
    <td class="tg-tgze">Median degree</td>
    <td class="tg-jbyd">312</td>
    <td class="tg-jbyd">576</td>
  </tr>
</tbody>
</table>

We can look at the degree distributions of the two networks.
<div class="row">
  <div class="column">
    <img src="/images/review_distribution.png" alt="Snow" style="width:100%">
  </div>
  <div class="column">
    <img src="/images/random_distribution.png" alt="Forest" style="width:100%">
  </div>
</div>
Both networks have around the same average degree, but their distributions vary. The degree distribution for the reviewer network is much more spread out, with degrees ranging from 8 to 5155, and skewed towards the left, indicating that smaller degrees are the most frequent. This is reflected in the median degree of the reviewer network, which is much lower than median degree of the random network.

For both networks we can compute the average clustering coefficient, which is a measure of the degree to which nodes tend to cluster together. According to Barabási[^1], one would expect a real-life network with N nodes and L edges to have much higher clustering coefficients than a random network of similar size. The average clustering coefficient for the reviewer network is x, while the average clustering coefficient for the random network is y. As expected, the reviewer network has a much higher average clustering coefficient than the random network! 

# <b>Product network</b>

As mentioned in the [Data description](data-description), each product has a list of related products that would be recommended to a user if they were to look at the product on Amazon. Additionally, each product also has the attribute "Categories". We hypothesise that this category attribute can be used to make a partitioning of the products. The products will be nodes in a network, and an edge between the nodes means that one product is a related product to the other. Only products with other category tags than "Grocery & Gourmet Food" were used in the network, so that every note does not belong to the same group.

![](/images/network_cats_tags.png)

The colors represent different categories or groups in the partitioning. The plots have circles some nodes which belong to the categories they represent.

We can take a closer look at some of the products in the network:

One of the more interesting areas is the island containing the product "B0033HGLTG" among others. This particular product is a coffee pad, and thus has the category "Beverages". Interestingly, the product "B009GCXEW4" is not a beverage, while all of its connected nodes appear to be. This product is in the category "Gourmet Gifts" category, and is a coffee pod holder. So while it is very related to the other products on the island, it is not in the same category. This phenomenon shows that related products are not nescessarily of the same category, which will weaken the communities in the network.

We now calculate the modularity of the category partitioning. The modularity is a measure for the quality of a partitioning, with a high number being good.

The modularity for the category partitioning is 0.4696 rounded to 4 decimals. This value indicates that the category is a decent partitioning, about on par with what we expected it to be. However, by using the Louvain algorithm to find a partitioning we can get a sense of how well the category partitioning actually did.

The Louvain partitioning has a modularity of 0.7591 rounded to 4 decimals.

We would expect it to find better communities than the category partitioning since the modularity is bigger.
We visualize the network to see:


![](/images/358louvain.png)

The most obvious difference is in the presence of nodes like "B009GCXEW4" which is connected to a cluster of mostly "Beverages" category products, but has a different category itself. The absence of these kind of nodes raises the modality of the partitioning. Another impactful change is within the center of the graph, where the nodes have been more cleanly split into groups, compared to the original graph where nodes with the "Beverages" category and the "Cooking & Baking" category were shuffled together.

It is quite clear that there is some overlap between communities in the two partitionings. As such, we want to make a confusion matrix to see which Louvain groups contain which categories.

![](/images/confusion358.png)

Making a confusion matrix for the two partitionings yeilds this somewhat incomprehensible table, since the Louvain split has 69 bins. This is due to the singleton nodes(the nodes that are not connected with any other nodes) each having their own group. Since singleton nodes are not particularly interesting for community analysis, and since they do not affect the modularity of a partitioning, the next step is to remove them all.

After doing this we get the following network for the category partitioning:

![](/images/306.png)

There are no changes to the communities(except the colors, which do not matter) with connections. As stated earlier the modularity does not change, since it only takes into account nodes that have edges. 

The louvain partitioning network looks like this:

![](/images/306louvain.png)

And with that we can create a more readable confusion matrix:

![](/images/confusion306.png)

Some of the large categories like "Cooking & Baking" are separated into multiple communities in the louvain split. This is likely due to them being shuffled in "Canned" and "Beverages" in the most dense areas of the network. Since the louvain split jsut wants the most interconnected communities, it makes sense that these categories would not stay intact. Conversely, the baby food category is all contained in a single Louvain community. This is due to it already being isolated in the category partitioning. In the Louvain partitioning, the baby food product now share community with 2 "Beverage" products and a "Canned" product. Likewise, there is also a "Beverage" island contained in Louvain community 14, with a single "Gourmet Gifts" product and a single "Candy & Chocolate" product.
[^1]: http://networksciencebook.com/chapter/3#clustering-3-9