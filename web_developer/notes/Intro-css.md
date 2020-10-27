# Materials
Code: 
- [CodePen repo week1](https://codepen.io/collection/noEQed/)
- [CodePen repo week2](http://codepen.io/collection/DVYVpB/)
- [CodePen repo week3](http://codepen.io/collection/XGowWM/)
  
Reading: [Building Your First Web Page](https://learn.shayhowe.com/html-css/building-your-first-web-page/)
# Week 1 
## CSS = cascading style sheet

In HTML:
```html
<h1 style = 'color:blue'>Styled Heading</h1>
```
    selector {
    	property: value;
    }
e.g.

```css
    h1 {
    	color: blue
    }
```

comment:` /* ..... */`
### Internal Style Sheet
Styling is defined within `<head>`

```html
<style>
	(css syntax)
</style>
```

### External Style Sheet
put rules in an external file
link to the style sheet is put in the head section



```html
<link rel='stylesheet' href='style.css'>
```
### "Cascading"
Browser default
***External* **style sheets
***Internal***  style (in the head section)
***Inline***I style (inside an HTML element)

### Rule precedence
the recent (last listed) css file

[css example - csszengarden](http://csszengarden.com "css example")

## Colors
### Color Convention
Names `blue, red`
Hexadecimal `#0000FF #FF0000`
RGB `(0,0,1)(1,0,0)`

### Check color contrast
[]()

## Styling  
**Font**
1. Font-family
Provide alternatives in case some browser does not support one font-family
2. `serif` fonts and `sans-serif` fonts **(better)**
3. font-style: normal, italic, oblique
4. font-variant: normal, small-caps
5. font-size: pixel, percentage (can be customized)
6. background-color
```css
h1, span{
		color:
		backrgound-color
}
```
7. text-align: left, right, center, justify
8. line-height: percentage

## Display and Visibility
(`<div>`)
Complementary Properties
- float
- Clear

### Overflow
- visible
- hidden
- scroll
- auto

# Week 2
## Box Model 
1. **Border**:   
specifies *style*, *width*, *color*
```css
div {
    border: solid 1px #CC00AA;
}
```
style:
none, dotted, solid .... 

3. **Margin**: space <u>*outside*</u> border

4. **Padding**: space <u>*between*</u> element and border

(example in ppt)

5. centering an element: `margin: 0 auto`

6. box-sizing: content-box/border-box

## Styling links and lists 
### Anchor links 
as text styling
1. botton
2. status  
a:link, a:visited, a:hover, a:focus, a:active (happen at the time when click)

Precedence:
- a:hover MUST come after a:link and a:visited
- a:active MUST come after a:hover

3. Styling lists
- list-style-type
- list-style-image

## Advanced Selectors
Follows DOM
- 1
- 2
- 3

**id Selectors**
one single element in DOM
```html
<div id="header">
```

**class selector**
identify an element in the DOM that is a part of a special class of items
```html
<img src='xx.jpg', class='thumb'>
```

classes vs ids
- syntax: .class | #id
- classes can be used multiple times, id is unique

narrowing
`p.main` paragraphs using main class
`header img.special` paragraph inside header has special class

expanding
combine elements with a comma: `p, h1, #main, .special`

Using Operators
`a[href='info.html']`
- `^`
- `$`
- `*`:applies to every element on the page
  
[Supplemental reading on complex selectors](http://learn.shayhowe.com/advanced-html-css/complex-selectors/)

QUIZ:
- You can have multiple classes applied to a single element.
- When a page is broken down into a DOM, the class information is stored in the tree.

## Browser Capabilities

Default style sheet (earlier than your style sheet)

[caniuse.com](http://caniuse.com)

add browser prefixes
- border-radius
- column-count


Setting background image
- [Setting Backgrounds & Gradients](http://learn.shayhowe.com/html-css/setting-backgrounds-and-gradients/)
- [Opacity](https://css-tricks.com/almanac/properties/o/opacity/)


# Week 3
## Pseudo-Classes
- link: `:link`, `:visited`
- user action: `:hover`
- forms(interfaces): `:enabled`, `:checked`
- structural/positional
- textual
- etc.

## Transitions
transition-property
transition-duration
transition-timing

Steps:
- define element
- transition
- pseudo class

using shortcuts (in one line)

## Transforms (status changes)
2D: translate, rotate, scale, skew, matrix

transform:scale(width, height)
transform:skew(x-angle,y-angle)

3D rotate
transform:rotate3D(x,y,z)

[OPTIONAL READINGS - Transitions, Transforms, and Animation](https://www.coursera.org/learn/introcss/supplement/kyViF/optional-readings-transitions-transforms-and-animation)

## Positioning
- static (default)
- relative
- absolute
- fixed 


QUIZ:  
Question 6
The style tag and the style attribute are interchangeable -- this means that you accomplish the same effect with both.   
**FALSE**

Q: Sometimes elements overlap one another. Which property specifies the stacking order of the elements? (A high value means it is more likely to be place in front of another.)  
A: z-index property

Static is not an option of 'position' property (but default choice).