<h1 align="center">Lexica.art API</h1>
<p align="center"><b>An easy-to-use reverse engineered Python API wrapper for Lexica.art</b></p>

# Usage
## Searching For Images Using The API
```python
from Lex import Lexica

lex = Lexica(query="icecream").images()
print(lex)
```
<b>It will return you a list with the image links</b>

## Generating Images Using The API
<b>You must have a registered account on [Lexica](https://lexica.art/) first.</b>

<b>Once you're registered you need the cookie from the site. To find the cookie open Inspect Tools then navigate to the `Network` Tab and start recording the requests. Generate an image and intercept the requests, there you'll find a request named `generator` open the requests and scroll down until you find the `cookie` parameter in the headers section of the request</b>

![Untitled](https://user-images.githubusercontent.com/88582190/229284905-18a12791-62d5-4277-853d-a346530cb223.png)

<b>Copy the entire cookie value and store it in a variable or a file.</b>

```python
from Lex import Lexica

cookie="YOUR COOKIE"

lex = Lexica(query="icecream",cookie=cookie).generate()
print(lex)
```
<b>It will return you a list with the image links</b>


### Additional Configurations
- <b>negativePrompt: Default to `None`</b>
- <b>guidanceScale: Default to `7`</b>
- <b>portrait: Default to `True` (If set to `False` will generate a landscape image with ratio (768,512))</b>

## Thank You
- <b>I hope you found this useful, If you did consider giving it a star <3</b>
