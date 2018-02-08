# CSS Grid

## Terminology
- Track: 
    This is the combination of column and row. It's basically the spaces between the items or more specifically its the start and end of a grid
- Explicit Track:
    These are the tracks that you created using grid-template-column. They show up as the dark dashed lines in the firefox dev tools
- Implicit Track:
    These are the tracks that are created when an item is shifted over when they exceed your explicit constraints.
- fr (fractional unit):
    unit used in grid to evenly divide a container. Its the measurement of left over space after the grid elements are layed out
        interesting note if you try to define rows using fr, the container must explicitly have a set height otherwise the browser won't know how to devide the rows 
- auto:
    Sizes the item based on its content. NOTE this will effect the whole row or column
- spaning:
    This increases the width of the item to span the ammount specified on the grid. CSS grid automatically adds more tracks when the if you span more than you have available

## Properties
- display: grid
    This much like flex is applied to the container element and passes the grid prop to it's children

- grid-template-column:
    This property is where you set the amount of columns and as well as their width

- repeat(n, u)
    This is a value used in conjunction with grid-template-column. Basically it takes the number of times you want to repeat something (n) and the units(px, em, rem, %, ect..) of the thing....
- grid-template-rows:
    This property is much like grid-template-columns except it sets the ammount of rows and their height
- grid-auto-rows:
    Sets the height of implicitly added rows
- grid-auto-columns:
    sets the width of implicitly added columns 
- grid-auto-flow:
    determines whether your implicit items are added as a row or column
- auto-fit:
    Makes enough columns to fit the items on the page
    will not create additional implicit tracks if there's free space left
- auto-fill:
    Makes enough columns to fit the items on the page and if theres any left over space it will create an additional number of implicit tracks to fill the rest
- minmax():
    this is used to wrap items. it takes two arguments the minimum an item's width or hight can me and the max. This will allow grid to determine at what point it should stack the items onto extra rows. USUALLY USED IN CONJUNCTION WITH auto-fit in order to make everything look neat.
- fit-content:
    this accepts a unit(px, em whatever) and constrains the item and the content of that item to that width or height depending if you're using it with grid-template-column/row
- areas:
    They're great!!!