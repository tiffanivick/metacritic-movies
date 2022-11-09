# metacritic-movies
This project uses Python and regular expressions to create a web scraper that searches for movie titles, dates, descriptions, metascores, and images in Metacritic. It gets the Metacritic url and constructs a list of movies from a particular year and page and then writes it to a csv file. It then reads the file and performs an analysis on the data.

The project is built using Python and Regual Expressions in Jupyter Notebook.

## Built With

![Visual Studio Code](https://img.shields.io/badge/Visual%20Studio%20Code-0078d7.svg?style=for-the-badge&logo=visual-studio-code&logoColor=white)
![Jupyter Notebook](https://img.shields.io/badge/jupyter-%23FA0F00.svg?style=for-the-badge&logo=jupyter&logoColor=white)
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-%23ffffff.svg?style=for-the-badge&logo=Matplotlib&logoColor=black)
![MongoDB](https://img.shields.io/badge/MongoDB-%234ea94b.svg?style=for-the-badge&logo=mongodb&logoColor=white)

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
- Seaborn
  
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

## License

Distributed under the MIT license. See `LICENS.txt` for more information.
