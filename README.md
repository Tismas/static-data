# static-data

Static JSON data hosted on GitHub Pages.

## Usage

Fetch the JSON data from:
```
https://tismas.github.io/static-data/data.json
```

### Example

```javascript
fetch('https://tismas.github.io/static-data/data.json')
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));
```

### CORS

GitHub Pages automatically serves files with appropriate CORS headers, allowing you to fetch the JSON data from localhost or any other origin.

## Data Structure

The `data.json` file contains an array of shape objects:

```json
[
  {
    "id": 1,
    "type": "square",
    "size": 30
  },
  {
    "id": 2,
    "type": "circle",
    "radius": 25
  },
  {
    "id": 3,
    "type": "rectangle",
    "width": 50,
    "height": 20
  }
]
```

## Local Testing

To test locally:

```bash
# Using Python
python -m http.server 8000

# Using Node.js
npx http-server

# Using PHP
php -S localhost:8000
```

Then open `http://localhost:8000` in your browser to see the index page and test the data endpoint.
