# DOCSS (Declaration Ordered CSS)
DOCSS (Declaration Ordered CSS) is an approach to writing CSS files which builds on the DRY CSS approach.

The **two** primary defining characteristics of DOCSS are that:

1. the style author groups elements and classes by style declaration, rather than grouping style declarations by element or class; and

2. the stylesheet is broken down into sub-sections, such that the entire document resembles a collection of smaller, self-contained stylesheets.

##Before starting DOCSS##

A couple of considerations before you adopt the DOCSS approach to stylesheet formatting. 

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
h1 {color: rgb(127,127,127);}
h1 {font-size: 24px; line-height: 36px;}
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
3. The stylesheet fragment above declares the `font-size` and the `line-height` of `h2` twice, which requires the human reader to perform the `cascade` in their own head.

**In Summary:** A concise stylesheet is the objective. But not at the cost of *maintainability* or *legibility*.

##URL list to plough through...##

- http://csswizardry.com/2013/07/writing-dryer-vanilla-css/
- https://www.youtube.com/watch?v=-cIAk3vDeBc
- http://johnpolacek.github.io/expressive-css/
- https://www.linkedin.com/pulse/scalable-modular-approaches-css-richard-omolo
- https://www.netguru.co/blog/8-rules-improve-css
- https://designshack.net/articles/css/5-steps-to-drastically-improve-your-css-knowledge-in-24-hours/
- https://vimeo.com/38063798
- http://www.creativebloq.com/css3/create-modular-and-scalable-css-9134351
- http://tympanus.net/codrops/2012/11/20/learning-principles-for-improving-your-css/
- https://css-tricks.com/forums/topic/dry-html-vs-oocss-approach-better-to-have-less-html-or-css-code/
- http://meiert.com/en/blog/20141009/css-dry-and-optimization/
- http://snook.ca/archives/html_and_css/are-you-single
- http://www.danylkoweb.com/Blog/top-10-css-bad-practices-FA
- https://speakerdeck.com/jlong/refactoring-css-programming-principles-for-designers
- https://www.advomatic.com/blog/front-end-code-review-fundamentals
- http://alchemyindesign.com/notes/2012/10/03/resources-for-modularizing-your-css.html
- http://j4n.co/blog/structuring-css
- http://sssslide.com/www.slideshare.net/jewlofthelotus/decoupling-the-frontend-through-modular-css
- https://css-tricks.com/keeping-breakpoints-dry/
- http://blog.mobnia.com/writing-modular-css-with-sass-and-bem/
- http://staging.keironlowe.co.uk/blog/writing-dryer-vanilla-css/
- http://www.mtlstate.com/confoo-2012-drying-css-for-brevity-unity-and-maintainability/
- http://docslide.us/internet/tech-headline-css-naming-conventions-improve-your-code-with-oocss-smacss-dry-and-bem.html
- http://www.awmcreative.com/notebook/speedy-modular-and-scalable-css/
- https://prezi.com/qlmjtdnzfhtj/css-architectures/
- http://www.getlinkyoutube.com/watch?v=-cIAk3vDeBc
- http://joshbroton.com/my-sass-less-css-practices-modularization-nesting-variables-mixins-etc/
- http://mathayward.com/modular-css-with-sass-and-bem/
- https://davidwalsh.name/starting-css
- http://www.impressivewebs.com/modular-css-media-queries-sass/
- http://mrmrs.io/writing/2016/03/24/scalable-css/
- http://derekmorash.com/work/css-architecture-and-semantics/
- http://www.intelligiblebabble.com/a-pattern-for-writing-css-to-scale
- http://red-badger.com/blog/2015/11/09/patterns-for-scaling-css/
- http://blog.chrismaxwell.com/keeping-your-css-code-dry
- https://mattstauffer.co/blog/organizing-css-oocss-smacss-and-bem
- https://vishnugopal.com/2007/08/10/dry-css/
- http://deepubalan.com/blog/2010/06/17/the-dry-principle-in-web-design/
- http://appendto.com/2014/04/oocss/
- https://www.quora.com/OOCSS-What-is-the-best-way-to-write-modular-and-scalable-CSS-OOCSS-SMACSS-BEM-or-DRY
- http://vanseodesign.com/css/dry-principles/
- https://vimeo.com/38063798
