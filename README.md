# graphqlGoClient
simple graphql client 👾 👾
# Installation
```go
go get github.com/sch00lb0y/graphqlGoClient
```
# Usage
```go
package main
import "sch00lb0y/graphqlGoClient"
import "fmt"

func main() {
    client:=graphqlGoClient.New("http://localhost/graphql")
    res,_:=client.Do(`
       user(id:"14MSE0052"){
       name
       friends
        }
      `)
    fmt.Println(string(res))
}
```
#note
you can write both `Query` and `Mutation` in `Do` method itself
