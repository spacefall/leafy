# leafy
## What's this?
Hi! This is leafy, an overcomplicated classless CSS framework/theme for (almost) everything, from blogs to simple web apps.
You can find a demo of most HTML5 elements [here](https://spacefall.github.io/leafy/demo.html).
### But why?
Simple: I'm tired of messing about with CSS and some pre-existing (classless) themes like [Sakura](https://github.com/oxalorg/sakura) feel restrictive as (imo) they're optimized for blogs. Other (still classless) frameworks like [Simple.css](https://simplecss.org) are better, but I still feel something could be done slightly better/different.

So that's why I spent the last few days messing about with CSS and ended up making a similar theme to Simple.css.

## Usage
Like other classless themes, leafy takes 0.1s to install, simply add the following line to you html document's head:
```html
<link rel="stylesheet" href="https://spacefall.github.io/leafy/leafy.min.css">
```
> You should always use the .min.css version unless you're modifying the theme

And you're done! You should also add the responsive meta tag if you want to make your website responsive but other than that there's nothing else you have to do.

leaf should work fine with any html document (markdown->html too, in fact this is the readme.md from the repo), some features require some modification though:
- For a snazzy header like the one in this page use a `<header>` tag at the start of the body, and inside use a `<h1>` tag:
  ```html
  <body>  
  <header>  
   <h1>Snazzy title</h1>  
   <p>Subtitle I guess</p>  
  </header>  
  </body>
  ``` 
- Same thing for the footer:
  ```html
  <body>  
  <header>  
   <h1>Snazzy title</h1>
  </header>  
  <footer>  
   <p>cool footer</p>  
  </footer>  
  </body>
  ``` 
- Navigation can also be added to the header in the following way:
  ```html
  <header>  
   <nav> 
       <ul>
           <li><a href="#url1">Item 1</a></li>
           <li><a href="#url2">Item 2</a></li>
       </ul>
   </nav>
  </header>
  ``` 
  **Note:** You should use a `<a>` tag (even not hyperlinked) to show a button, other elements don't have any effect currently
- You can also add a dropdown by nesting a list inside an item:
  ```html
  <nav>
      <ul>
          <li><a href="#url1">Item 1</a></li>
          <li>  
           <a>Drop-down</a>  
           <ul>
               <li><a href="#url2">Item 2</a></li>
               <li><a href="#url3">Item 3</a></li>
           </ul>
          </li>
      </ul>
  </nav>
  ``` 

## Theming
All of leaf's colors, border properties (thickness, radius) and animation time can be customized since they're just CSS variables:
```css
/* colors from everforest https://github.com/sainnhe/everforest */
:root {
    --bg: #F3EAD3;  /* main background */
    --bg-light: #EAE4CA;  /* lighter bg, used in header and some elements (mainly text) */
    --bg-dark: #E5DFC5;  /* darker bg, used in footer and other (mostly input) elements */
    --sep: #E5DFC5;  /* an even lighter shade of the background used for borders */
    --text: #5C6A72;  /* main text color */
    --text2: #939F91;  /* secondary text color, used, for example, in disabled elements */
    --accent1: #8DA101;  /* primary accent color, the brightest one */
    --accent2: #93B259;  /* secondary accent, used mostly on hover of elements */
    --accent3: #A7C080;  /* tertiary accent, the darkest one, used mostly when elements are clicked */
    --on-accent: #E5E6C5; /* text color to use on --accent1 color */

    --rad: .4rem;  /* rounded corner radius */
    --thick: .135rem;  /* thicker border thickness */
    --thin: .1rem;  /* thinner border thickness */
    --anim: .3s;  /* time for transitions */
}  
```
By default, leaf also supports dark mode, if you want to edit those colors just change them inside a `@media (prefers-color-scheme: dark)` block.


## Thanks
[everforest](https://github.com/sainnhe/everforest) for a great color scheme which leaf uses.  
[Sakura](https://github.com/oxalorg/sakura) and [Simple.css](https://simplecss.org) for being great CSS themes and indirectly being great resources for building a theme.  
[modern-normalize.css](https://github.com/sindresorhus/modern-normalize) for giving decent defaults that work (basically) everywhere.

