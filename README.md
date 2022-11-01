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
from typing import Union

from fastapi import FastAPI

app = FastAPI()


@app.get("/")
def read_root():
    return {"Hello": "World"}


@app.get("/items/{item_id}")
def read_item(item_id: int, q: Union[str, None] = None):
    return {"item_id": item_id, "q": q}
```