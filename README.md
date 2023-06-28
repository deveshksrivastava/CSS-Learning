# CSS-Learning-

[Edit on StackBlitz ⚡️](https://stackblitz.com/edit/web-platform-dkqtho)

# short cut
div>ul>li*3>lorem1
bd+ gives border
#box1 will creat div with class="box1"

when we take margins/border/padding we need to decrease the height and width of the div.

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

shadow
   box-shadow x-axis | y-axis | blur | range | color;
   box-shadow: 0px 0px 10px 5px red;

   text-shadow: 0px 0px 10px 5px red; /* x-axis | y-axis | blur | color; */

overflow
  overflow: hidden | scroll;
  overflow-y: scroll;
  overflow-x: hidden;

transform
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
column
    <!-- https://www.youtube.com/watch?v=zg_mmC8THqM -->
    column-count: number - devide the page into columns
    column-gap: number - this will be the gap between columns.
    column-fill: balance | auto , this effect columns-count so need to manage the height;
    column-rule: number - this will be the make the border
    column-span: number - merge 2-3 columns
    column-width: number

opecity (0-1) 0.1,0.25,0.99
transition:1s the change in opacity will show after 1 second

resize both
    the box can be resized , px or %

text-indent: number | %
    thie will start indent of paragraphs text 

Animation               //https://www.youtube.com/watch?v=zg_mmC8THqM
  making shift and then change color and with time and which direction and how long

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

