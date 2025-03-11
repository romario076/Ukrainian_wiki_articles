# Ukrainian Wikipedia Articles Interactive Visualization
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
Under "wireframe": true
```
getPosition: (d) => d.coordinates,
pickable: true,
onClick: (info) => {
  if (info.object && info.object.Article) {
    window.open(info.object.Article, "_blank"); // Open URL in a new tab
  }
},
```

Also replace controller by:
```
controller: {
  dragPan: true,
  scrollZoom: true,
  touchZoom: true,
  touchRotate: true
}
```

Here it is possibe manually interact with wiki data using SPARQL:
* https://query.wikidata.org/

<hr>

### Interactive Map
https://raw.githack.com/romario076/ukrainian_wiki_articles/refs/heads/main/index.html

Hove over data points to see additional information or click to open respective wikipedia page.

### Example:
<img width="530" alt="image" src="https://github.com/user-attachments/assets/c1c63ccf-46c4-482f-8cdf-ac08716b23f3" />

<hr>

#### To change cursor type to more convenient add this to html file:
```
#deck-container {
  width: 100vw;
  height: 100vh;
  cursor: crosshair !important; /* Force crosshair cursor */
}

#deck-container canvas {
  z-index: 1;
  background: none;
  cursor: crosshair !important; /* Ensure crosshair for interactive elements */
}
```


