# mGrid - A Simple SASS/CSS Grid System - v 1.0.0.0

mGrid is an extremely simple SASS grid system, free for anyone to use.

In order to change the amount of padding in the SASS, simply edit the `$padding` variable at the top of the mGrid.scss file.

# How To Use

To use the grid system, you simply need to create a parent container with the class `container` and then use the appropriate `col_` class. The grid uses a 12-column system, so `col_3` is 1/4 width, `col_6` is 1/2 width, `col_9` is 3/4 width and `col_12` is full width. The cols will fill the width of the *parent* container that they are in.

For example:

``` HTML
<section class="container">
  <div class="col_6">
    I am 1/2 width
  </div>
  
  <div class="col_6">
    I am 1/2 width
  </div>
</section>
```
will create a full-width container with two 50% divs inside it. If you want to then split the first div into a 1/4 and 3/4 then you simply use the appropriate `col_` inside the div, for example:

``` HTML
<section class="container">
  <div class="col_6">
    <div class="col_3">
      I am the first 1/4 of my parent col_6 div.
    </div>
    
    <div class="col_9">
      I am the other 3/4 of my parent col_6 div.
    </div>
  </div>
  
  <div class="col_6">
    I am 1/2 width
  </div>
</section>
```
will create two rows. The first row will have a div taking up the first quarter, and a div taking up the other 3 quarters. The second row will just contain a div taking up the first half of the row.

## Helper Classes
There are helper classes that you can use for purposes outside of the main grid `col_` system.

### `.padding-<size>` or `.padding-<loc>-<size>` / `.margin-<size>` or `.margin-<loc>-<size>`
To use the padding and margin helper classes, simply add it to your element to add the appropriate padding or margin. Here are some examples:

``` CSS
.padding-10 {
	padding: 10px
}

.padding-left-15 {
	padding-left: 15px;
}

.margin-right-5 {
	margin-right: 5px;
}
```

# TODO
- Add `mGrid-px`, a pixel-based extension to the core mGrid. This will allow for pixel based responsive design.
- Add ability to add own row classes
- Add `.padding-global` to use the global padding value
- Add the ability to show/hide elements on certain device sizes via classes.
- Add `mGrid-ui` to include better styled UI items such as:
  - Dropdowns
  - Multi-Select Dropdowns
  - Tabs
