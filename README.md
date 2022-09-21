# RequestsEx

HTTP request building, parsing, executing & timing all in one! Make a performant HTTP request with 1 line of code.

## Usage

- Create a new Python file
- Import the entire RequestsEx module
- Use the testing.py & example below to build an easy request

## Example

Behind the scenes the library will take the basic info you give & build a full HTTP payload.
```cs
# make a new request object (view testing.py for all options)
newReq = eRequest('post', 'https://example.com', data={
  'myData': '123'
})

# execute the request
newResp = newRew.do()

# output the response
print(newResp.text)
```

## TODOs

- Proxy support using pysocks
- Support for passing in your own socket objects
