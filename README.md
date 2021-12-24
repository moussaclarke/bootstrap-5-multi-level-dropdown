# Bootstrap 5 Multiple Level Dropdown.

Use standard Bootstrap markup without having to add any extra CSS styles and classes, it's just like having native support.

Everything mentioned in https://v5.getbootstrap.com/docs/5.1/components/dropdowns/ should just work. You can use any of the css classes and js methods/events/options.

Multi level dropdowns are a very common use case and relatively easy to implement in Bootstrap 5, seems like a glaring omission in core - this package solves that.

## Usage

### Base
Just add the js after your bootstrap js:

```html
<script src="https://example.com/bootstrap5-multi-level-dropdown-browser.js"></script>
```

Or include the module if you're using a build tool.

```json
/* In your package.json deps */
"bootstrap5-multi-level-dropdown": "github:moussaclarke/bootstrap-5-multi-level-dropdown"

```js
import 'bootstrap5-multi-level-dropdown/js/bootstrap5-multi-level-dropdown-module.js';
```

#### Base Example
```html
...
<div class="dropdown mt-3">
    <button class="btn btn-secondary dropdown-toggle" type="button" id="dropdownMenuButton" data-bs-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
        Dropdown button
    </button>
    <div class="dropdown-menu" aria-labelledby="dropdownMenuButton">
        <a class="dropdown-item" href="#">Action</a>
        <!-- level #2 -->
        <div class="dropdown dropend">
            <a class="dropdown-item dropdown-toggle" href="#" id="dropdown-layouts" data-bs-toggle="dropdown" aria-haspopup="true" aria-expanded="false">Layouts</a>
            <div class="dropdown-menu" aria-labelledby="dropdown-layouts">
                <a class="dropdown-item" href="#">Basic</a>
                <a class="dropdown-item" href="#">Compact Aside</a>
                <div class="dropdown-divider"></div>
                <!-- level #3 -->
                <div class="dropdown dropend">
                    <a class="dropdown-item dropdown-toggle" href="#" id="dropdown-layouts" data-bs-toggle="dropdown" aria-haspopup="true" aria-expanded="false">Custom</a>
                    <div class="dropdown-menu" aria-labelledby="dropdown-layouts">
                        <a class="dropdown-item" href="#">Fullscreen</a>
                        <a class="dropdown-item" href="#">Empty</a>
                        <div class="dropdown-divider"></div>
                        <a class="dropdown-item" href="#">Magic</a>
                    </div>
                </div>
                <!-- /level #3 -->
            </div>
        </div>
        <!-- /level #2 -->
        <a class="dropdown-item" href="#">Something else here</a>
    </div>
</div>
...
<script src="https://example.com/bootstrap5-multi-level-dropdown-browser.js"></script>
```
### Hover
If you want a hover trigger, you can just add class and some custom styles to reduce spacing to avoid triggering mouseleave.
```css
.dropdown-hover-all .dropdown-menu,
.dropdown-hover > .dropdown-menu.dropend {
    margin-left: -1px !important;
}
```
or include the `bootstrap5-multi-level-dropdown-hover.css` file.

Then, add classes for dropdown elements;
```html
<div class="dropdown-hover-all">
  <!-- .dropdown elements -->
</div>
<div class="dropdown dropdown-hover">
  <!-- toggle and menu elements -->
</div>
```
#### Hover Example
```html
<link rel="stylesheet" href="https://example.com/bootstrap5-multi-level-dropdown-hover.css" />
...
<div class="dropdown-hover-all">
  <!-- .dropdown elements -->
</div>
<div class="dropdown dropdown-hover">
  <!-- toggle and menu elements -->
</div>
...
<script src="https://example.com/bootstrap5-multi-level-dropdown-browser.js"></script>
```

### jsfiddle

Here is a demo: https://jsfiddle.net/dallaslu/mvk4uhzL/
