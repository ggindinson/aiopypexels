
## An asynchronous wrapper for Pexels API based on aiohttp, which additionally allows to download photos in any of avaliable resolutions.


## Installation

Install aiopypexels with pip

```bash
  pip install aiopypexels
```
    
## Examples

Searching photos by query 
```python
from aiopypexels import AioPexels
from aiopypexels.types import PhotoSearchResponse

api = AioPexels(API_KEY)

async def get_photos_by_query(query: str) -> PhotoSearchResponse:
    response = await api.get_photos_by_query(query)
    print(response.total_results)  # 498

```
Getting photo by ID 
```python
from aiopypexels import AioPexels
from aiopypexels.types import Photo

api = AioPexels(API_KEY)

async def get_photo_by_id(id: int) -> Photo:
    photo = await api.get_photo_by_id(id)

```
Downloading photo by ID 
```python
from aiopypexels import AioPexels

api = AioPexels(API_KEY)

async def download_photo_by_id(query: str) -> PhotoSearchResponse:
    response = await api.download_photo_by_id(photo_id=9999, destination = './photos/test.jpeg', quality='original')

```


## Links
[![](https://img.shields.io/github/stars/ggindinson?label=GitHub%20Repo&style=social)](https://github.com/ggindinson/aiopypexels)

[Latest Version](https://pypi.python.org/pypi/aiopypexels/)


## Feedback

I would be very pleased for a star :-)