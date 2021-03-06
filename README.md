# pyrest-client

[![Build Status](https://travis-ci.org/gnehcc/pyrest-client.svg?branch=master)](https://travis-ci.org/gnehcc/pyrest-client)
[![Coverage Status](https://coveralls.io/repos/iamwucheng/pyrest-client/badge.svg?branch=master&service=github)](https://coveralls.io/github/iamwucheng/pyrest-client?branch=master)
<a href="https://raw.githubusercontent.com/iamwucheng/pyrest-client/master/LICENSE"><img src="https://img.shields.io/hexpm/l/plug.svg"></a>

### A simple python rest client based on requests.

pyrest-client gives you a way to call restful api in chaining mode. 

## Usage

We can use this code snippet get top 250 movies on [Douban](http://www.douban.com):

```
from pyrest_client import RestClient

RestClient('https://api.douban.com').v2.movie.top250.get()
```

Also easy to update info using `POST` method:

```
from pyrest_client import RestClient

payload = {
        'book': 'xxxx',
        'title': 'this is a title',
        'content': 'this is content',
        'rating': 5
    }
    
RestClient('https://api.douban.com').v2.book.reviews.post(data=payload)
```

It is just a abstract level based on requests, giving you ability to generating right api address in a chaining mode and call the service at the end to return the result. you can assign everything when you are using requests to call service.


## License

pyrest-client is released under the Apache License. See LICENSE for details.

