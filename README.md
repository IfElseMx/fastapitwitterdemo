# fastapitwitterdemo
Twitter and Fast API - Learning  functions
## Installation

Use the package manager [pip](https://pip.pypa.io/en/stable/) to install foobar.

```bash
# Create VENV

python3 -m venv venv

# Active VENV

source env/bin/activate

# Install Requirements 

pip3 install -r requirements.txt

# Start Uvicorn ASGI (Asynchronous Server Gateway Interface) 

uvicorn main:app --reload

```

## Usage

Edit and explore functions in main.py  🚀

```python

# Tweets

# Show  all tweets
@app.get(
    path="/",
    response_model=List[Tweet],
    status_code=status.HTTP_200_OK,
    summary="Show all tweets",
    tags=["Tweets"]
)
def home():
    return {"Twitter API": "Working!"}

# Post a tweet


@app.post(
    path="/post",
    response_model=Tweet,
    status_code=status.HTTP_201_CREATED,
    summary="Post a tweet",
    tags=["Tweets"]
)
def post():
    pass
```