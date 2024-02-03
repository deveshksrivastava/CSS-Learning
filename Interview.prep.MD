CSS Learning 

### [Postion](https://twitter.com/Prathkum/status/1367469980527255554/photo/1)  
  - Static - Default, goes by the page flow, top to bottom 
  - Relative 
          - simmiler like static, but allow to change by right,left,top,bottom and z-index
          - Remove from the document flow
          .child {
              postion:relative;
              top:10px; //genrally not used
         }
  - Absolute
         - used for to change by right,left,top,bottom, to postion of page
         - parent continer having relative, sticky, fixed
         - child have absolute
         - Remove 1 element from the dom flow but rest sticks
  - Fixed
         - simmiler to absolute
         - stick to HTML full body, stick to same postion when scroll, ex: suppost at top, when we scroll with go along the page and will not show
         - simmiler to absolute
  - Sticky
         - fixed + relativw
         - parent relative, child- fixed, stick to the postion, and always show even when we scroll down.
### FlexBox
    - Continer & Items
    - Continer
          - based on main axis(row) and cross access(Column)
          - create 1 div continer and insied 4 items
          .container {
              disply: flex;
              justify-contect: center;  //space-around (x-axis)
              align-item: flex-start/center; //(cross-axis)
              align-contect: center; //rarely used, used for multiline
              flex-wrap: wrap;
              height: 700px
         }
### Overflow - hide scrollbar
