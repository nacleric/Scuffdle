# Scuffdle

Wordle-clone for teaching Javascript

## Browser specific knowledge
These are functions I needed to use to communicate with our 6x5 wordle Grid

https://developer.mozilla.org/en-US/docs/Web/API/Document/querySelector
 `.querySelector()`
 Grabs a Dom element by either its ID or Class. Because it only grabs a single Dom element I usually use it for ID's

 https://developer.mozilla.org/en-US/docs/Web/API/Document/querySelectorAll
 `.querySelectorAll()`
 Same as querySelector but returns a list of DOM elements. Because it grabs multiple I usually use it for Classes


The document object allows you to access each HTML element. If I want to grab each row of the wordle board I'll use
`let rows = document.querySelectorAll(".scuffdle-row");`
row0

row1

row2

..

row5

Sometimes you might not want access to every HTML element. Alot of our game logic involves doing checks on a specific row.

`let cols = rows[currentRow].querySelectorAll(".scuffdle-col")`

On this line I wanted to grab only the 5 columns of the currentRow I'm on.

- row0
    - col0 col1 ..
- row1
    - col0 col1 ..

- row2 (  row[2].querySelectorAll(".scuffdle-col")  )
    - col0 col1 col2 col3 col4 <---- I only want these columns

..

- row5
    - col0 col1 ..
