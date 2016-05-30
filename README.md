# SECSS (Sequentially Expressed CSS)
SECSS (Sequentially Expressed CSS) is an approach to writing CSS files which builds on the DRY CSS approach.

The **two** primary defining characteristics of SECSS are that

i) the stylesheet is broken down into sub-sections, such that the entire document resembles a collection of smaller, self-contained stylesheets; and

ii) the style author groups elements and classes by style declaration, rather than grouping style declarations by element or class.

**Three Best Practices for Keeping Stylesheets Concise**

1) Wherever possible, use CSS shorthands.

eg.

Instead of:

h1 {
border-width: 2px;
border-style: solid;
border-color: rgb(191,191,191);
}

use:

h1 {border: 2px solid rgb(191,191,191);}

Instead of:

h1 {

}

use:

h1 {background: }



2)

3)

**One consideration for Keeping Stylesheets Maintainable** 
