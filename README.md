<center><h1>go Modules, Packages, Files</h1></center>

[!NOTE] This repo is just for understanding how does the modules, packages and files works in go.

## problem statement. 
 - create a module with two packages.
    - greeter, welcome 
 - greeter package has a greeter.go file.
 - welcome package has a welcome.go file.

### understand how modules, packages and files works. 

```
  greeter
  |___greeter.go 
  |
  welcome
  |____ welcome.go 

```


### Run Command

```bash 
go mod init github.com/primegen-git/go-greeter 
```

> [!TIP]
> github.com/primegen-git/go-greeter  -> this just tell go where to look for this module.
> Think of this as a canonical name for your module.

> Now, If you want to import the code from the **welcome** package or **greeter** package

```go 

// main.go file 
pakcage main 

import (
  "github.com/primegen-git/go-greeter/greeter" >[!TIP] module name + sub-package name.
  "github.com/primegen-git/go-greeter/welcome"
)

func main() {
  welcome.Say()
  greeter.Greet() 
}
```
```
```


> If you want to use it in the local machine, in some other go project, 
> this structure is going  to be same just you have to point **module-name** -> local path

