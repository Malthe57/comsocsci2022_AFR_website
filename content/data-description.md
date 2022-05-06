---
title: Data description
prev: "/"
next: network-analysis
---


The dataset consists of product reviews and metadata of products in the "Grocery and Gourmet Food" category on Amazon and was collected by researchers at UCSD.

The original reviews dataset has 142.8 million reviews spanning from May 1996 - July 2014. However, we use only use a subset of the dataset where all users and items have at least 5 reviews in the "Grocery and Gourmet Food" category, called food 5-core. The food 5-core dataset is 108 MB and contains 151,254 reviews, with each review having 9 attributes:

- <code>reviewerID</code> - ID of the reviewer, e.g. A2SUAM1J3GNN3B
- <code>asin </code> - ID of the product, e.g. 0000013714
- <code>reviewerName </code> - name of the reviewer
- <code>helpful </code> - helpfulness rating of the review, e.g. 2/3
- <code>reviewText </code> - text of the review
- <code>overall </code> - rating of the product
- <code>summary </code> - summary of the review
- <code>unixReviewTime </code> - time of the review (unix time)
- <code>reviewTime </code> - time of the review (raw)

The metadata dataset contains metadata for 171,761 products in the "Gorcery and Gourmet Food" category and is 182 MB. Each product has 9 attributes:

- <code>asin </code> - ID of the product, e.g. 0000031852
- <code>title </code> - name of the product
- <code>price </code> - price in US dollars (at time of crawl)
- <code>imUrl </code> - url of the product image
- <code>related </code> - related products (also bought, also viewed, bought together, buy after viewing)
- <code>salesRank </code> - sales rank information
- <code>brand </code> - brand name
- <code>categories </code> - list of categories the product belongs to

The two datasets can be downloaded <a href="http://jmcauley.ucsd.edu/data/amazon/links.html" target=_blank >here</a>


Below is a summary of the identified categories that we have worked with, and how many products and review text tokens there are in each category.
<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  overflow:hidden;padding:10px 5px;word-break:normal;}
.tg th{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  font-weight:normal;overflow:hidden;padding:10px 5px;word-break:normal;}
.tg .tg-2qwx{background-color:#ffffff;border-color:#000000;color:#333333;text-align:center;vertical-align:top}
.tg .tg-mums{background-color:#ffffff;border-color:#000000;font-weight:bold;text-align:center;vertical-align:top}
.tg .tg-jbyd{background-color:#ffffff;border-color:#000000;text-align:center;vertical-align:top}
.tg .tg-vhtn{background-color:#ffffff;border-color:#000000;text-align:center;vertical-align:middle}
</style>
<table class="tg">
<thead>
  <tr>
    <th class="tg-2qwx"><span style="font-weight:bold">Category</span></th>
    <th class="tg-mums"><span style="font-weight:bold">Number of products</span></th>
    <th class="tg-mums"><span style="font-weight:bold">Number of review tokens</span></th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-mums">Baby foods</td>
    <td class="tg-jbyd">21</td>
    <td class="tg-vhtn">37,730</td>
  </tr>
  <tr>
    <td class="tg-mums">Beverages</td>
    <td class="tg-jbyd">95</td>
    <td class="tg-vhtn">72,767</td>
  </tr>
  <tr>
    <td class="tg-mums">Breakfast foods</td>
    <td class="tg-jbyd">14</td>
    <td class="tg-vhtn">7,766</td>
  </tr>
  <tr>
    <td class="tg-mums">Candy &amp; Chocolate</td>
    <td class="tg-jbyd">23</td>
    <td class="tg-vhtn">8,798</td>
  </tr>
  <tr>
    <td class="tg-mums">Canned</td>
    <td class="tg-jbyd">61</td>
    <td class="tg-jbyd">45,528</td>
  </tr>
  <tr>
    <td class="tg-mums">Cooking &amp; baking</td>
    <td class="tg-jbyd">120</td>
    <td class="tg-jbyd">85,303</td>
  </tr>
  <tr>
    <td class="tg-mums">Fresh flowers &amp; Live Indoor Plants</td>
    <td class="tg-jbyd">1</td>
    <td class="tg-jbyd">257</td>
  </tr>
  <tr>
    <td class="tg-mums">Gourmet gifts</td>
    <td class="tg-jbyd">1</td>
    <td class="tg-jbyd">246</td>
  </tr>
  <tr>
    <td class="tg-mums">Snack Foods</td>
    <td class="tg-jbyd">22</td>
    <td class="tg-jbyd">12,227</td>
  </tr>
</tbody>
</table>
