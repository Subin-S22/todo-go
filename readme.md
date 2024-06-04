## anonymous structs

it is for only if we are not using a struct again

```go
mycar := struct {
Make string
Model string
}{
Make:'make name',
Model: 'model number'
}
```

## methods in go

```go
// struct are powerful when used as variable and functions
type rect struct {
  width int
  height int
}
func (r rect) area() int{
  return r.width * r.height
}

r := rect{
  width:40,
  height:40
}

fmt.Println(r.area())
```

## error handling

it helps us to directly handle the errors for a particular
use cases

```go
func user(){
  user, err := getUser()
  if err != nil {
    //handle the error here
  }
  //handle user details here

  image, err := getUserImage(user.id)
  if err != nil {
    //handle the error here
  }
  //handle image details here

}
```

### Variadic functions

```go
func sum(nums ...int) int{
  total := 0
  for i:=0;i<len(nums);i++ {
    total += nums[i]
  }
  return total
}

func main(){
  total := sum(1,2,3);
  fmt.Println(total);
}
```
