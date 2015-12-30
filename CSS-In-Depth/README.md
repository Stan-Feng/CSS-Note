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
```css
UI Attribute Selector
input[type=checkbox]:checked + label {
  color: red;
  font-family: cursive;
  font-weight: bold;
}

Structural UI Selector
tr:nth-of-type(odd) td:nth-of-type(odd) {
  background-color: #900; color: #fff;
}
tr:nth-of-type(even) td:nth-of-type(even) {
  background-color: #aaa; color: #fff;
}

Negation Selector
tr:not(:nth-child(1)) {
  background-color: orange;
  font-weight: bold;
}
```
    - :target -- You can use this prop making switching tab, hidden, focus, etc.
    - :hover:
    - :active:
    - :focus
  - Pseudo Elements
    - ::