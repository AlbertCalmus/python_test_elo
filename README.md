# Hands-on Python :  Squash Elo

## Requirements

### Python
Install Python by following this link https://www.python.org/downloads/release/python-3102/, use Windows installer (64-bit)

### Pip
Use the following command in a terminal prompt to install pip

```
python -m ensurepip --upgrade
```

### Virtual environment
To avoid global installation it is recommended to use a virtual environment, use the following commands to create one and activate it
```
mkdir python_test_elo
cd python_test_elo
```
```
python -m venv venv
```
```
venv\Scripts\activate.bat
```

### Libraries
Run the following command to install required Python libraries
```
pip install jupyter-lab pandas numpy
```

### Jupyter
Run the following command to spin up a local Jupyter Lab server
```
jupyter lab
```

## Instructions

### Input files
##### `players.csv`
Contains a list of players with the following format
```csv
name,elo
Alice,1725
Bob,1250
Charlie,1533
```

##### `games.csv`
Contains a list of games with the following format
```csv
player1,player2,winner
Alice,Bob,1
Bob,Charlie,2
Alice,Charlie,1
```

### Output files
##### `updated_players.csv`
Contains a list of players with their updated elo after taking into account all games described in `games.csv`. The update formula for elo can be found [here](https://metinmediamath.wordpress.com/2013/11/27/how-to-calculate-the-elo-rating-including-example/), we will use a K-factor `K=32`
