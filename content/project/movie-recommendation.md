+++
# Date this page was created.
date = 2016-04-27T00:00:00

# Project title.
title = "Movie Recommendation"

# Project summary to display on homepage.
summary = "Discover the potential value of movie and its ranking from each person."

# Optional image to display on homepage (relative to `static/img/` folder).
image_preview = "bubbles.jpg"

# Tags: can be used for filtering projects.
# Example: `tags = ["machine-learning", "deep-learning"]`
tags = ["Data Mining", "Machine Learning"]

# Optional external URL for project (replaces project detail page).
external_link = ""

# Does the project detail page use math formatting?
math = false

# Optional featured image (relative to `static/img/` folder).
[header]
image = "headers/bubbles-wide.jpg"
caption = "My caption :smile:"

+++

Developed a User-based Collaborative Filtering Algorithm with Spark to help recommend suitable movies to customers. By doing so, I discovered frequent movie item sets by implementing Apriori and SON Algorithms.

A-priori Algorithm is used for frequent item set mining and association rule learning. It proceeds by identifying the frequent individual items in the database and extending them to larger and larger item sets as long as those item sets appear sufficiently often in the database.

For example: There is a transaction itemsets record looks like as below:

<table>
	<tr><td>Itemsets</td></tr>
	<tr><td>{1,2,3,4}</td></tr>
	<tr><td>{1,2,4}</td></tr>
	<tr><td>{1,2}</td></tr>
	<tr><td>{2,3,4}</td></tr>
	<tr><td>{2,3}</td></tr>
	<tr><td>{3,4}</td></tr>
	<tr><td>{2,4}</td></tr>
</table>

<table>
    <tr>
        <td>Item</td>
        <td>Support</td>
    </tr>
    <tr>
    	<td>{1}</td>
    	<td>3</td>
    </tr>
    <tr>
    	<td>{2}</td>
    	<td>6</td>
    </tr>
    <tr>
    	<td>{3}</td>
    	<td>4</td>
    </tr>
    <tr>
    	<td>{4}</td>
    	<td>5</td>
    </tr>

</table>

All the itemsets of size 1 have a support of at least 3, so they are all frequent.

When size becomes bigger, our support will change as well.

<table>
	<tr>
		<td>{1,2}</td>
		<td>3</td>
	</tr>
	<tr>
		<td>{1,3}</td>
		<td>3</td>
	</tr>
	<tr>
		<td>{1,4}</td>
		<td>2</td>
	</tr>
	<tr>
		<td>{2,3}</td>
		<td>3</td>
	</tr>
	<tr>
		<td>{2,4}</td>
		<td>4</td>
	</tr>
	<tr>
		<td>{3,4}</td>
		<td>3</td>
	</tr>
</table>

We have thus determined the frequent sets of items in the database, and illustrated how some items were not counted because one of their subsets was already known to be below the threshold.

The power of this is:

You can find those items that tend to be purchased together more frequently than other items — the ultimate goal being to get shoppers to buy more. Together, these items are called itemsets.
Skillset: Python, Spark, Hadoop


