# handlebars-precompilation-demo

The article is present on [SitePoint](http://bit.ly/1DRmfKe).

A demo to show how handlebars precompilation works

1. keep all the template files with `.handlebars` extension inside the `templates folder`.
2. In the root folder run `handlebars templates/ -f templatesCompiled.js`
3. You will get a compiled `templatesCompiled.js` in the root directory.
4. Insert the runtime handlebars and the compiled js file

```html
<script src="handlebars.runtime.js"></script>
<script src="path/to/templatesCompiled.js"></script>
```

5. Access the template of `demo.handlebars` by using

```javascript
var context = {
	"name":"Ritesh Kumar",
	"occupation" : "Developer"
}

var templateScript = Handlebars.templates.demo(context);

$(body).append(templateScript);
```

6. Run `index.html` on the browser to see the resultant html.

That's it.
