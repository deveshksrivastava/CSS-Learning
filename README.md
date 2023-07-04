# CSS-Learning-

[Edit on StackBlitz ⚡️](https://stackblitz.com/edit/web-platform-dkqtho)

# short cut
```
.box1 will create div with class="box1"
#box1 will create div with ID="box1"
div>ul>li*3>lorem1
bd+ gives border

()  - grouping
div{Hello $} -> <div>Hello 1</div>
+   - adding (div+div+div) create div in same level 
^^^ - Make level up
```

# selector 
check in the psudocode.html file
  
  .className
  ```
    -> used multiple times
    i.e <div class="continer">
    .container {
      direction: flex
    } 
```
  #id
  ```  -> used only one time
    i.e
    <div id="user_id">
    #user_id {
      direction: flex
    } 
```

# selector type
## Simple Selector
``` 
 simple         - body {}, h1{} 
 class          - .container {}
 id             - #box{}
 universal      - * {  margin:0 } // apply to all
 grouping       - h1, h2, p { color: #000000 }
```

## Combinators Selector
```
      <div class="box">
        <p>HI<p> 
        <p>Hello</p>
        <div>
          <p>Helo<p>
          <p class="pbox">Hel1o<p>
           
 1. depndent slector(space)  -> div p { color: #00000 }  
    // all the color change in all the p tag
 2. child selctors (>)       -> div.box > p { color: #000000 }
    // color change in the fist child of p tag only
    ul > li { color: #000000 }

   ****************************************     
      <h1>Hellow</h1>
        <p>lorem5</p>
        <p>lorem5</p>
        <p>lorem5</p>
  3. Adjacent Sibling Selector(+) -> h1 + p { color: #000000 }
    // h1 and next p will be colored
  4. General Sibling Selector(~)  -> 
    h1 ~ p { color: #000000 }  => To selct all the  <p> element comes after <h1>
    p ~ img  =>To select all <img> elements that come anywhere after <p> elements,

    h1 ~ p {
        background-color: #333;
        padding: .5em;
    }

    <article>
      <h1>A heading</h1>
      <p>I am a paragraph.</p> //make this background color
      <div>I am a div</div>
      <p>I am another paragraph.</p> //make this bg color
    </article>
    
```

## Atribute Selctor
```
  <input type="text" name="" value="">
  <input type="text" name="" value="">
  <input type="email" name="" value="">

  //this will make all the above 3 elements red
  input { 
    border: 1px solid #000000 
  }
 
 // this will make the first 2 elements red
  input[type="text"] { border: 1px solid #000000 }
```

## psudu slector 
  ```
  div class="box"
    p
    p
    p
    p

    // this will make the first paragrap red
    div.box p:first-child { 
      background : #000000
    } 

    // this will make the last  paragrap red
    div.box p:last-child { 
      background : #000000
    } 

    // this will make the 2 nd paragrap red
    div.box p:nth-child(2) { 
      background : #000000
    }
  ```
## psudu element slector 
```
  <p>this is the tester element</p>
    ::after     ::first-letter  ::selection
    ::before    ::first-line    ::placeholder
    p::first-letter { color = red } // this will make the first letter red
```



# nav bar in one direction
```
  nav ul li {
    display: inline; // make in to columns other way is flex, grid
    margin-right: 10px;
  }
```
# display              
WsCube Tech-(https://www.youtube.com/watch?v=kIASoZjmCG0&t=450s)
MDN https://developer.mozilla.org/en-US/docs/Web/CSS/display check example

            
    ## display: none    (TO HIDE) 
 
    ## display: inline  (ONE SINGLE LINE, DIV->SPAN, WITHOUT MARGIN)
      1. (li) make all of them in column (ONE SINGLE LINE)
      2. make **div** to **span** span - this behave like text to make like div, why? 
      3. in span WIDTH/MARGIN DON'T WORKS
      note - this can also be done with display:flex, but can be changed with flex-direction:column
 
    ## display:block   (SPAN -> DIV, WITH MARGIN)
      1. fix and make **span** to **div**,
      2. This makes in 2 line 
      3. div breaks not span
      2. Make div and margin, padding works 
     
    ## display:inline-block 
      1. this will make like span in 1 single line but width/margin works 
      2. (imp : you can use the width/margin)
    
    ## display: list-item; 
      1. makes the property as list, comes in new line, show the dot on the text, 
      2. now you can use all the list property like list-style-position: inside;, 
         and for span working as div 


when we take margins/border/padding we need to decrease the height and width of the div.

# RGB color
R 255
G 255
B 255
background-color: rgb(255,255,255)
rgb
   rgb(0,0,0) - black
   rgb(255,255,255) - white
   rgb(255,255,0) -yellow
   rgb(255,0,0) -red
   rgb(0,0,255) -blue
   rgb(0,255,0) -green
   rgb(255,0,255) -pink
   first is red, second is green, third is blue
rgba
   [a] used from opecity/how much can we fade, 0.9 max fade out
   a= 0 - 1, 0.1,0.2,0.25,0.50
   rgba(255,255,255)

# shadow
   box-shadow x-axis | y-axis | blur | range | color;
   box-shadow: 0px 0px 10px 5px red;

   text-shadow: 0px 0px 10px 5px red; /* x-axis | y-axis | blur | color; */

# overflow
  overflow: hidden | scroll;
  overflow-y: scroll;
  overflow-x: hidden;

# transform
  <!-- transform -->
  works only 1 time
  transform: translate(10px, 10px); // this will shift the box
    transform: translateX(100px);
    transform: translateY(100px);

    <!-- skew(deg|turn) -->
    transform: skew(30deg, 30deg); // turn in 30 degrees clock

    <!-- rotate(deg|turn) work on x,y,x axia-->
    transform: rotate(30deg, 30deg); // turn in 30 degrees clock

    <!-- scale(number) zoom-->
    transform: scale(2.5); // inlarge 2.5 times 

# column
    <!-- https://www.youtube.com/watch?v=zg_mmC8THqM -->
    column-count: number - devide the page into columns
    column-gap: number - this will be the gap between columns.
    column-fill: balance | auto , this effect columns-count so need to manage the height;
    column-rule: number - this will be the make the border
    column-span: number - merge 2-3 columns
    column-width: number

# opecity (0-1) 0.1,0.25,0.99
```
transition:1s the change in opacity will show after 1 second

resize both
    the box can be resized , px or %

text-indent: number | %
    thie will start indent of paragraphs text 
```

# Animation              
 https://www.youtube.com/watch?v=zg_mmC8THqM
 ``` making shift and then change color and with time and which direction and how long

  @keyframes - this is the bock and how much to change time,duration

  animation-name: ""
  animation-fill-mode: top/dwon
  animation-timing-function: animation
  animation-direction - everse/normal
  animation-itration-count - how many times
  animation-delay 0 - how long to delay animation
  animation-duration 0 - how long animation
  animation - short hand property
  Example
    .box {
      widht:200px; height200px;
      background:red;
      position:absolute;
      top:0px;
      left:0px;
   
      <!-- animcation: box 5s 10; -->
         
      animation-name: box;
      animation-duration:5s;
      animation-delay:2s; //animcatino willl start after 2s 
      animation-itteration-count:10; //infinite loop
      animation-fill-mode: fowords | backword | both //color change from red to blue
      animation-direction: reverse | alternate | alternate-revrese | normal

      timming
      linear
      easy
      easy-in
      ease-out
      ease-in-out
    }

    @keyframes box {
      <!-- devide the 5s in % to do the animation -->
      0% {
        top: 0px;
        left: 0px;
        background:red;
      }
      25% {
        top: 0px;
        left: 400px;
        background:yellow;
      }
      50% {
        top: 400px;
        left: 400px;
        background:blue;
      }
      75% {
        top: 0px;
        left: 0px;
        background:blue;
      }
      <!-- 100% should and become same property -->
      100% {
        top: 0px;
        left: 0px;
        background:red;
      }
    }
```

# TO DO :
1. How to make it to the left in the header
```

     flex-direction: row;
     justify-content:space-between;
     
      we removed above and used below and because in case of 3rd elemnet aligh will not work like logout button after nav and used 
      
      .navclassName{
         margin-left: auto; // this will push to the right
      }

       <nav class="navclassName">
          <ul>
            <li><a href="">home 1</a></li>
            <li><a href="">home 2</a></li>
          </ul>
        </nav>
```

2. how to use the min-height 
```
    .continer {
      border: 3px solid red;
      min-height: 100vh;
       /* two approch 1 is min-height and max-height: 100vh; overflow: scroll;*/
      /* max-height: 100vh;
      overflow: scroll; */
      /* max-height: 80vh;
      overflow: hidden;  */
      /* this will hide all the content: ; */
    }

```

3. remove line, * and hide
```
  text-decoration: none; //remove line no <a>
  list-style-type: none; //remove * on the list item
  display: none; //hide 
  display: inline-block; - make in single line like span
```

4. Make center in Flexbox and Grid
 ``` align-items: center;```
5. Making footer to the bottom of the page ``` position: fixed; bottom: 0;``` insted use in main ``` min-height: 100vh; ```, as the page grows footer will be at bottom.
6. Making grid in mobile on 1 line ``` grid-template-columns: 1fr;``` in media query for mobile and in deskto 
```  
        display: grid;
        grid-template-columns: repeat(2, 1fr);
 ```
 
