# pongorenderer
Minimal Pongo2 renderer for Echo that just works.

# Usage  
## Installation  

`go get "github.com/siredwin/pongorenderer/renderer"`

The next step is define renderer and call it

```go
func main() {
  MainRenderer = renderer.Renderer{Debug:true}
  
  // Echo instance
  e := echo.New()
  
  //Use renderer
  e.Renderer = MainRenderer
}

```
somewhere in the program use `Render`  
```go
func index(c echo.Context) error {
	data := pongo2.Context{}
	return c.Render(http.StatusOK, "page.html", data)
}

```
