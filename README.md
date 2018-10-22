# bldrs

Simple builder classes to construct html and svg in client-side runtime.

The Bldr class is used to create html/svg tags with attributes and nested elements. 
## example

```{javascript}
let svg = new Bldr("svg").att("version", "1.1")
	.att("xmlns", "http://www.w3.org/2000/svg")
	.att("xmlns:xlink", "http://www.w3.org/1999/xlink")
	.att("align", "center").att("width", 10).att("height", 10)
	.elem(new Bldr("rect").att("width", 8).att("height",8)
		.att("fill","green"));

displayDiv.innerHTML = svg.build();
```
