# RequestsEx

HTTP request building, parsing, executing & timing all in one! Make a performant HTTP request with 1 line of code.

## Usage

- Create a new Python file
- Import the entire RequestsEx module
- Use the testing.py & example below to build an easy request

## Example

Behind the scenes the library will take the basic info you give & build a full HTTP payload.
```cs
import time
from RequestsEx import *

# make timing object for when the request will connect/fire (optional)
myTiming = RequestTiming(
  connectAt   = round(time.time()+3), 
  sendAt      = round(time.time()+5)
)

# make a new request object (view testing.py for all options, only method & url are required)
newReq = eRequest('post', 'https://example.com', data={
  'myData': '123'
}, timing=myTiming)

# execute the request
newResp = newRew.do()

# output the response
print(newResp.text)
```

## TODOs

- Proxy support using pysocks
- Support for passing in your own socket objects
