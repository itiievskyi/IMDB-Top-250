# IMDB Top 250 movies

### Parser

This is simple parser written on Python using:
  * *requests*
  * *bs4 (BeautifulSoup)*
  * *re*
  * and *pandas*
  
The aim is to create a dataframe containig a detailed data about Top 250 movies.
The list can be found here: [Top 250 as rated by IMDb Users](https://www.imdb.com/chart/top).

Parser creates a list of movie personal page links and then handles each of them to fill the dataframe.
The search requests are combination of **BeautifulSoup** and **regex** syntax:

```movies.at[n, 'Duration'] = soup.find('time', {'datetime':re.compile('[a-zA-Z0-9]*')}).get_text().strip()```

The result is the table 250\*8:

![Table #1](/images/1.png)

### Data manipulation
In this section I use `.style` method to change the Dataframe look (creating in-cell bars and changing alignment).

![Table #2](/images/2.png)

### Dataframe plot
Let's see how many marks left IMDB users for movies, released in different years?

![Table #3](/images/3.png)

### How to use
Just open the **IMDB-Top-250.ipynb** in your Jupyter Notebook.

Make sure that **Python3**, *requests*, *bs4*, *pandas* and *re* are installed on your system.


### Enjoy!
