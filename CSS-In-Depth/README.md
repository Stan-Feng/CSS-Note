## CSS In Depth

### Selectors
  - [Browser Support]( http://standardista.com)
  - Basic Selectors  
```css
#myId
.myClass
div
```
  - Relational Selectors
```css
ul li (descendant selector, matches nested <li>)
ol > li (direct child selector, matches<li> in <ol> not nested <ul>)
li.myClass + li (adjacent sibling)
li.myClass ~ li (general sibling selector)
```
  - Attributes Selectors
```css
element[attribute] (Select elements containing the named attribtue)
img[alt] {}
  <img src ='image.jpg' alt = 'accessible'>
form input[type] {}
  <input type=date>
form input [type="date"] {}
  <input type=date>
p[data-attr|= "en"] {} /*<p = data-attr-lang = "en-us"> <p data-attr-lang = "en-uk"> HTML5 dataset attribute*/
p[attr^=val] /*Regular Expression*/
```  
  - Pseudo Class Selectors
UI Attribute Selector
```css
input[type=checkbox]:checked + label {
  color: red;
  font-family: cursive;
  font-weight: bold;
}
```

  - Structural UI Selector
```css  
tr:nth-of-type(odd) td:nth-of-type(odd) {
  background-color: #900; color: #fff;
}
tr:nth-of-type(even) td:nth-of-type(even) {
  background-color: #aaa; color: #fff;
}
```
  - Negation Selector
```css  
tr:not(:nth-child(1)) {
  background-color: orange;
  font-weight: bold;
}
```
    - :target -- You can use this prop making switching tab, hidden, focus, etc.
    - :hover:
    - :active:
    - :focus
  - Pseudo-class **select** elements already exist.
  - Pseudo-elements create "faux" elements you can style


## Generated Content
  - Generated Content is created by CSS, which is **NOT** a part of DOM.
```css
p::before {
  content: 'bananas';
  font-weight: bold;
}
p::after {
  content: 'apples';
  font-weight: bold;
}
```
  - [CSS Tricks of Generated Content]( http://css-tricks.com/examples/ShapesOfCSS/)
  - Generated Content can be manipulated in CSS, JavaScript can't.
  - Values for content: none, normal, string, image, counter
  - Usually can be used
    - as background image sprite
    - as notification
    ```css
    a[href^=http]:hover {
      position: relative;
    }
    a[href^=http]:hover::after {
      content: attr(href);
      position: absolute;
      top: 1em;
      left: 0;
      background-color: black;
      color: white;
      line-height: 1px;
    }
    ```
    - as triangles
    ```css
    .triangle {
      border-radius: 10px;
      position: relative;
      padding: 20px;
      background-color: red;
      white;
    }
    .triangle::after {
      position: absolute;
      content: '';
      width: 0;
      height: 0;
      border: 20px solid transparent;
      border-top-color: red;
      bottom: -39px;
      left: 20px;
    }
    ```