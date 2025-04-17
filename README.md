# Ukrainian Wikipedia Articles Interactive Visualization
This repository contains a python code which extracts locations of birth and death of ukrainians which have an wikipedia article. 
This application takes into account wikipedia pegaes where specified nationality or affiliation to Ukraine.

In ukrainians_wiki_articles.ipynb possible to create an application with intercative visualization maps where are possible to see a distrubution and hover over points to see detailed information.
Use zoom, scrolling and hover over points to interact with map.

Application contains three pages:
 - Народження (page with interactive map with distribution of birth location, if it specified)
 - Смерть (page with interactive map with distribution of death location, if it specified)
 - Статистика (page with statistics by gender, distance between birth and death locations)


To reproduce results, firsly run:
```
pip install -r requirements.txt
```

Launch jupyter notebook from cmd:
```
jupyter notebook
```

Here it is possibe manually interact with wiki data using SPARQL:
* https://query.wikidata.org/

<hr>

### Interactive Map
https://raw.githack.com/romario076/Ukrainian_wiki_articles/refs/heads/main/wiki_application.html

Hove over data points to see additional information or click to open respective wikipedia page.

### Example:
<img width="955" alt="image" src="https://github.com/user-attachments/assets/317dafc4-cb5b-4806-8773-9db3f91fd78c" />

<hr>

```


