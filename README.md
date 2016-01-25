# row<sup>n</sup> grid system
The new way to use grid system


## Grid system
The best grid system to work with. It's flexible and works for any type of layout.

Starting with parent element as it plays main role here. We have to know how many children we want to be in the container.

So we can set it by naming the class `.row` and number which sets children quantity. For example `.row5` is the container which has 5 elements, each divided **20%** wide. In `.row8`, we'll have children divs **12.5%** wider and so on.

It works for children `<div>`, `<li>`, `<td>` elements and `.cell` classes. Like this:

    .row5
        & > div
        & > div
        & > .cell
        & > .cell
        & > div

    ul.row3
        & > li
        & > li
        & > li

and, of course make them **nested**, like this:

    section.row4
        & > div
        & > div.row2
            & > div
            & > div
        & > .cell
        & > ul.cell.row3
            & > li
            & > li
            & > li

**To increase child elements width** you need to use `.cell` + number class on this element. For example `cell3`. So, it works like this:

    .row5
        & > div
        & > div.cell3                   - this takes 3x more space then usual div
        & > div

    table
        & > tr.row4
            & > td
            & > td.cell2
            & > td

#### Spacing for the grid
To prevent spacing by left and right sides or inside cells use following classes:
    .row7
        &.no-padding                    - sticks cells on eachother
        &.side-padding                  - fits grid width by left and right side on the container
        &.twice-padding                 - makes padding 2x wider than default

#### Other grid features
You may use other features as well

    row2.float.nofloat                  - this feature (you'll meet this below) works here as well.
