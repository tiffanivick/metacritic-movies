# metacritic-movies
This project uses Python and regular expressions to create a web scraper that searches for movie titles, dates, descriptions, metascores, and images in Metacritic. It gets the Metacritic url and constructs a list of movies from a particular year and page and then writes it to a csv file. It then reads the file and performs an analysis on the data.

The project is built using Python and Regual Expressions in Jupyter Notebook.

## Getting Started

Imports used to run this program: 
- re
- urlib3
- certifi
- json
- pymongo
- time
- pandas
- matplotlib (pyplot and FormatStrFormatter)
  
To install in terminal: 
1. Open terminal 
2. path\\to\\project\\file: pip3 install {package to install} 

## How To Use

Connect to MongoDB
```
with open("/fileLocation/credentialsFileName.json") as f:
  data = json.load(f)
  mongo_connection_string = data ['mongodb']
```

Retrieve the data in your MongoDB collection
```
client = pymongo.MongoClient(mongo_connection_string, tlsCAFile=certifi.where())
db1_database = client['databaseName']
metacritic_data = db1_database['collectionName']
```

Get the Metacritic url 
```
url = "https://www.metacritic.com/browse/movies/score/metascore/year/filtered?year_selected=(year)&sort=desc&view=detailed&page=(page)"
```


