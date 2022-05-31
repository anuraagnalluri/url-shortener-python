# URL Shortener with FastAPI

[https://github.com/tiangolo/fastapi](https://github.com/tiangolo/fastapi)


```sh
$ cd src
$ pip install -U pip && pip install -r requirements.txt
$ uvicorn app.main:app --host 0.0.0.0 --port 8000 --reload
```

Using [curl](https://curl.haxx.se)

To shorten a link:
```sh
$ curl -X POST -d '{"url": "https://google.com"}' -H "Content-Type: application/json" http://localhost:8000/api/shorten | jq .
{
  "short_link": "Nw4IY0Y"
}
```

To access a shortened link, point your browser to http://localhost:8000/Nw4IY0Y
