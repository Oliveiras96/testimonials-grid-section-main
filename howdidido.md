# Developing notes

## HTML structure

structure the information of the person:

```HTML
<div class="testimonial-card item">

    <div class="profile-card">

        <div class="profile-header">

            <img>
            <div class="author-name">
            </div>

            <div class="stats">
            </div>
        </div>

        <div class="testimonial">
        </div>
    </div>
</div>
```

## Layout desktop

For ths layout i used the CSS grid system. Any `div` that has the property `display` set to `grid` will behave as a grid. It is possible to use this system to build table like layout pages. In this case, all the direct children of the grid-container div will automatically become grid items.

To position every grid-item in his place, there is many ways. grid-items ocupy one single column and row as standard, but is possible to make it ocupy as many columns and rows we want. The way used here was to explicit tell how many and where the items should be placed using the `grid-column` and `grid-row` property.

```HTML

<style>
    .grid-container {
        display: grid;
    }

    /* begin on column 1 and span 2 column*/
    .item1 {
        grid-column: 1 / span 2;
        grid-row: 1;
    }

    .item2 {
        grid-column: 2;
        grid-row: 1;
    }

    .item3 {
        grid-column: 4;
        grid-row: 1 / span 2;
    }

    .item4 {
        grid-column: 1 ;
        grid-row: 2;
    }

    .item5 {
        grid-column: 2 / span 2;
        grid-row: 2;
    }  
</style>    

<div class="grid-container">
    <div class="grid-item item1">
    </div>
    <div class="grid-item item1">
    </div>
    <div class="grid-item item1">
    </div>
    <div class="grid-item item1">
    </div>
    <div class="grid-item item1">
    </div>
</div>
