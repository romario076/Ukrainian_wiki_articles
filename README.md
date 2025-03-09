# Ukrainian_wiki_articles
This repository contains a python code which extracts locations of birth of ukrainians which have an wikipedia article.

In ukrainians_wiki_articles.ipynb possible to create a intercative visualization map where are possibel to see a distrubution and hover over points to see detailed information.
Use zoom, scrolling and hover over points to interact with map.

To reproduce results, firsly run:
```
pip install -r requirements.txt
```

Launch jupyter notebook from cmd:
```
jupyter notebook
```

To make points clickable neccessary add the following code under the Layer dictionary in .html file
```
getPosition: (d) => d.coordinates,
pickable: true,
onClick: (info) => {
  if (info.object && info.object.Article) {
    window.open(info.object.Article, "_blank"); // Open URL in a new tab
  }
},
```

Here it is possibe manualy iteract with wiki data using SPARQL:
* https://query.wikidata.org/

<hr>

### Example:
<img width="530" alt="image" src="https://github.com/user-attachments/assets/c1c63ccf-46c4-482f-8cdf-ac08716b23f3" />



