# SECSS (Sequentially Expressed CSS)
SECSS (Sequentially Expressed CSS) is an approach to writing CSS files which builds on the DRY CSS approach.

The **two** primary defining characteristics of SECSS are that

i) the stylesheet is broken down into sub-sections, such that the entire document resembles a collection of smaller, self-contained stylesheets; and

ii) the style author groups elements and classes by style declaration, rather than grouping style declarations by element or class.

##Before starting SECSS##

A couple of considerations before you to start to explore SECSS and discover how comfortable and enjoyable it can be. 

###Keeping Stylesheets Concise: Three Best Practices###

** 1) Where possible, use *CSS shorthands* **

*eg.*

Instead of:

``` css
h1 {
border-width: 2px;
border-style: solid;
border-color: rgb(191,191,191);
}
```

use:

``` css
h1 {border: 2px solid rgb(191,191,191);}
```

Instead of:

``` css
h1 {
background-color: rgb(127,0,0);
background-image: url('/assets/theme/elements/heading-logo.png');
background-repeat: no-repeat;
background-position: right top;
}
```

use:

``` css
h1 {background: rgb(127,0,0) url('/assets/theme/elements/heading-logo.png') no-repeat right top;}
```


** 2) Where possible, group related CSS declarations which consistently appear together **

** 3) Where possible, group related CSS elements and classes which consistently share the same declarations **

###Keeping Stylesheets Maintainable: One Consideration###
