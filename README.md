# API Basejump: URL Shortener microservice

## User stories

1. I can pass a URL as a parameter and I will receive a shortened URL in the JSON response.
2. If I pass an invalid URL that doesn't follow the valid http://www.example.com format, the JSON response will contain an error instead.
3. When I visit that shortened URL, it will redirect me to my original link.

## Creation sample

### Valid URLs
```
https://tan-surl.herokuapp.com/new/https://www.google.com 
https://tan-surl.herokuapp.com/new/http://freecodecamp.com/news
```

will output
```
{ "original_url": "https://www.google.com", "short_url": "https://tan-surl.herokuapp.com/1" }
{ "original_url": "http://freecodecamp.com/news", "short_url": "https://tan-surl.herokuapp.com/2" }
```

### Invalid URLs
```
https://tan-surl.herokuapp.com/new/aaa
```

will output
```
{ "error":"URL invalid" }
```

## Usage sample

### Valid URLs
```
https://tan-surl.herokuapp.com/1
```

will redirect to
```
https://www.google.com
```

### Invalid URLs
```
https://tan-surl.herokuapp.com/bbb
```

will output
```
{ "error":"No short url found for given input" }
```

## License

N/A