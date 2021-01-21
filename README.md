# url-shortener
url-shortener takes long url as JSON body to a POST Request and returns a short url. It uses Rebrandly APIs to shorten the url

# To run the code
1. Clone the repo
2. cd url-shortener
3. go build main.go
4. ./main

Once API server is up and running, it will start listening on port 8080

# Send the POST Request
You can use any HTTP Client to send POST request along with long url in JSON Body

```
{
	"original_url":"https://www.youtube.com/watch?v=7EvwIw4gIyk"
}

```
# USING CURL
```
curl localhost:8080 -d '{"original_url":"https://www.youtube.com/watch?v=7EvwIw4gIyk"}'
original url : https://www.youtube.com/watch?v=7EvwIw4gIyk
shorten url : rebrand.ly/xmbs20t

```
# Console output
```
INFO[0091] reading request body...
INFO[0091] original long url: https://www.youtube.com/watch?v=7EvwIw4gIyk
INFO[0091] creating request to send to rebrandly api...
INFO[0091] sending request to rebrandly api...
INFO[0092] getting response from rebrandly api...
INFO[0092] checking response status... 200 OK
INFO[0092] reading response body...
INFO[0092] extracting shorten url...
INFO[0092] original url : https://www.youtube.com/watch?v=7EvwIw4gIyk
INFO[0092] shorten url : rebrand.ly/xmbs20t
```
