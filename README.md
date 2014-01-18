# Requests.jl

#### HTTP for Julians.

## Quickstart

```
julia> Pkg.clone("https://github.com/forio/Requests.jl")

julia> using Requests
```

### Make a request

```
get("http://httpbin.org/get")
post("http://httpbin.org/post")
put("http://httpbin.org/put")
delete("http://httpbin.org/delete")
options("http://httpbin.org/get")
```

### Add query parameters

```
get("http://httpbin.org/get"; query = { "title" => "page1" })
```

### Add data

```
post("http://httpbin.org/post"; data = { "id" => "1fc80620-7fd3-11e3-80a5-7995390c4a5e" })
```

### Set headers

```
post("http://httpbin.org/post"; headers = { "Date" => "Tue, 15 Nov 1994 08:12:31 GMT" })
```

### Inspect responses

```
type Response
    status::Int
    headers::Headers
    data::HttpData
    finished::Bool
end
```