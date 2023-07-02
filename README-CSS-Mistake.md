# Css mistake
1. adding width=100%, for div,p,, h1-h6, table, form, article,main,footer
    above are block elements that don't require as they will take there own space of width
    block elements are those elements that are displayed as blocks and take up the full width available by default

2. people just declaring 
    display : flex;
    flex-direction : column; // don't do any thing, normail flow like div

3. people in card flex-basic: 33% (3 columns), 50%(2 cols), 
    fix is to use flex-basis: 100%, for make to 2, 3 columns, it will take it automatically
    div.card1>card.imge+p>div>imge+p

4. Using px for 0  - margin: 10px 0 20px
5. Using color : i.e red, blue, green, yellow
6. Not using shorthand notation : i.e 
7. Repeting code, not define symantics elemetn
8. Define 1 h1 and for other use the color i.e h1 > p + h1(class)