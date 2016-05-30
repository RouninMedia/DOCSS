# SECSS (Sequentially Expressed CSS)
SECSS (Sequentially Expressed CSS) is an approach to writing CSS files which builds on the DRY CSS approach.

The **two** primary defining characteristics of SECSS are that:

1. the style author groups elements and classes by style declaration, rather than grouping style declarations by element or class; and

2. the stylesheet is broken down into sub-sections, such that the entire document resembles a collection of smaller, self-contained stylesheets.

##Before starting SECSS##

A couple of considerations before you to start to explore SECSS and discover how comfortable and enjoyable it can be. 

###Concise Stylesheets: Three Best Practices###

**1) Where possible, use *CSS shorthands***

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


**2) *Similarly*, where possible, group *related* CSS style declarations which consistently appear together**

Instead of:

``` css
h1 {
color: rgb(127,127,127);
}

h1 {
font-size: 24px;
}

h1 {
line-height: 36px;
}
```

use:

``` css
h1 {color: rgb(127,127,127); font-size: 24px; line-height: 36px;}
```

**3) *Then*, where possible, group *related* CSS elements and classes which consistently share the same style declarations**

Instead of:

``` css
h1 {color: rgb(127,127,127); font-size: 24px; line-height: 36px;}
h2 {color: rgb(127,127,127); font-size: 18px; line-height: 27px;}
h3 {color: rgb(191,191,191); font-size: 18px; line-height: 27px;}
```

use:

``` css
h1, h2 {color: rgb(127,127,127);}
h3 {color: rgb(191,191,191);}

h1 {font-size: 24px; line-height: 36px;}
h2, h3 {font-size: 18px; line-height: 27px;}

```

###Keeping Stylesheets Maintainable & Legible: An Important Consideration while Following the 3 Concise Stylesheet Best Practices Above###

The objective of having SECSS on your website is not just to keep your styles relatively concise, but also clearly legible and highly maintainable. Concision is important, but it's not intended to be a consideration which overrides all others .

Reviewing the last example above, it would be *even more* concise to write:

``` css
h1,h2{color:#888;font-size:24px;line-height:36px;}
h2,h3{font-size:18px;line-height:27px;}
h3{color:#bbb;}
```
but, there are arguably 3 problems with this - the first two relating to *stylesheet maintainability* and the last relating to *stylesheet legibility*:

1.
2.
3. The stylesheet fragment above declares the `font-size` and the `line-height` of `h2` twice, which requires the human reader to perform the `cascade` in their head.

**In Summary:** A concise stylesheet is the objective. But not at the cost of *maintainability* or *legibility*.
