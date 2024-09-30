# Go generic lazy

```shell
go get -u github.com/jace996/lazy
```

```go
import (
    "context"
    "github.com/jace996/lazy"
)

type A struct {
	
}

lazyA := lazy.New[*A](func(ctx context.Context) (*A, error){
	return &A{}
})
a,_ := lazyA.Value(context.Background())
```