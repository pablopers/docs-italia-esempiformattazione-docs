This is a set of tests for pandoc. Most of them are adapted from John
Gruber’s markdown test suite.

#. .. rubric:: Headers
      :name: headers

   #. .. rubric:: Level 2 with an `embedded link <file:///url>`__
         :name: level-2-with-an-embedded-link

      #. .. rubric:: Level 3 with *emphasis*
            :name: level-3-with-emphasis

         #. .. rubric:: Level 4
               :name: level-4

            #. .. rubric:: Level 5
                  :name: level-5

   .. rubric:: Level 1
      :name: level-1

   2. .. rubric:: Level 2 with *emphasis*
         :name: level-2-with-emphasis

      2. .. rubric:: Level 3
            :name: level-3

with no blank line

Level 2
-------

with no blank line

Paragraphs
==========

Here’s a regular paragraph.

In Markdown 1.0.0 and earlier. Version 8. This line turns into a list
item. Because a hard-wrapped line in the middle of a paragraph looked
like a list item.

Here’s one with a bullet. \* criminey.

| There should be a hard line break
| here.

Block Quotes
============

E-mail style:

   This is a block quote. It is pretty short.

This should not be a block quote: 2 > 1.

And a following paragraph.

Code Blocks
===========

Code:

---- (should be four hyphens)

sub status {

print "working";

}

this code block is indented by one tab

And:

this code block is indented by two tabs

   These should not be escaped: $ \\ > [ {

6. .. rubric:: Lists
      :name: lists

   4. .. rubric:: Unordered
         :name: unordered

Asterisks tight:

-  asterisk 1

-  asterisk 2

-  asterisk 3

Asterisks loose:

-  asterisk 1

-  asterisk 2

-  asterisk 3

Pluses tight:

-  Plus 1

-  Plus 2

-  Plus 3

Pluses loose:

-  Plus 1

-  Plus 2

-  Plus 3

Minuses tight:

-  Minus 1

-  Minus 2

-  Minus 3

Minuses loose:

-  Minus 1

-  Minus 2

-  Minus 3

   5. .. rubric:: Ordered
         :name: ordered

Tight:

1. First

2. Second

3. Third

and:

1. One

2. Two

3. Three

Loose using tabs:

1. First

2. Second

3. Third

and using spaces:

1. One

2. Two

3. Three

Multiple paragraphs:

1. Item 1, graf one.

   Item 1. graf two. The quick brown fox jumped over the lazy dog’s
   back.

2. Item 2.

3. Item 3.

   6. .. rubric:: Nested
         :name: nested

-  Tab

   -  Tab

      -  Tab

Here’s another:

1. First

2. Second:

   -  Fee

   -  Fie

   -  Foe

3. Third

Same thing but with paragraphs:

1. First

2. Second:

   -  Fee

   -  Fie

   -  Foe

3. Third

   7. .. rubric:: Tabs and spaces
         :name: tabs-and-spaces

-  this is a list item indented with tabs

-  this is a list item indented with spaces

   -  this is an example list item indented with tabs

   -  this is an example list item indented with spaces

   8. .. rubric:: Fancy list markers
         :name: fancy-list-markers

(2) begins with 2

(3) and now 3

    with a continuation

    iv. sublist with roman numerals, starting with 4

    v.  more items

        A. a subsublist

        B. a subsublist

Nesting:

A. Upper Alpha

   I. Upper Roman.

      6. Decimal start with 6

         c. Lower alpha with paren

Autonumbering:

1. Autonumber.

2. More.

   1. Nested.

Should not be a list item:

M.A. 2007

B. Williams

Definition Lists
================

Tight using spaces:

.. raw:: html

   <div class="DefinitionTerm">

apple

.. raw:: html

   </div>

red fruit

.. raw:: html

   <div class="DefinitionTerm">

orange

.. raw:: html

   </div>

orange fruit

.. raw:: html

   <div class="DefinitionTerm">

banana

.. raw:: html

   </div>

yellow fruit

Tight using tabs:

.. raw:: html

   <div class="DefinitionTerm">

apple

.. raw:: html

   </div>

red fruit

.. raw:: html

   <div class="DefinitionTerm">

orange

.. raw:: html

   </div>

orange fruit

.. raw:: html

   <div class="DefinitionTerm">

banana

.. raw:: html

   </div>

yellow fruit

Loose:

.. raw:: html

   <div class="DefinitionTerm">

apple

.. raw:: html

   </div>

red fruit

.. raw:: html

   <div class="DefinitionTerm">

orange

.. raw:: html

   </div>

orange fruit

.. raw:: html

   <div class="DefinitionTerm">

banana

.. raw:: html

   </div>

yellow fruit

Multiple blocks with italics:

.. raw:: html

   <div class="DefinitionTerm">

*apple*

.. raw:: html

   </div>

red fruit

contains seeds, crisp, pleasant to taste

.. raw:: html

   <div class="DefinitionTerm">

*orange*

.. raw:: html

   </div>

orange fruit

   { orange code block }

Multiple definitions, tight:

.. raw:: html

   <div class="DefinitionTerm">

apple

.. raw:: html

   </div>

red fruit computer

.. raw:: html

   <div class="DefinitionTerm">

orange

.. raw:: html

   </div>

orange fruit bank

Multiple definitions, loose:

.. raw:: html

   <div class="DefinitionTerm">

apple

.. raw:: html

   </div>

red fruit

computer

.. raw:: html

   <div class="DefinitionTerm">

orange

.. raw:: html

   </div>

orange fruit

bank

Blank line after term, indented marker, alternate markers:

.. raw:: html

   <div class="DefinitionTerm">

apple

.. raw:: html

   </div>

red fruit

computer

.. raw:: html

   <div class="DefinitionTerm">

orange

.. raw:: html

   </div>

orange fruit

1. sublist

2. sublist

HTML Blocks
===========

Simple block on one line:

foo

And nested without indentation:

foo

bar

Interpreted markdown in a table:

This is *emphasized*

And this is **strong**

Here’s a simple block:

foo

This should be a code block, though:

<div>

foo

</div>

As should this:

<div>foo</div>

Now, nested:

foo

This should just be an HTML comment:

Multiline:

Code block:

<!-- Comment -->

Just plain comment, with trailing spaces on the line:

Code:

<hr />

Hr’s:

Inline Markup
=============

This is *emphasized*, and so *is this*.

This is **strong**, and so **is this**.

An `emphasized link <file:///url>`__.

**This is strong and em.**

So is **this** word.

**This is strong and em.**

So is **this** word.

This is code: >, $, \\, \\$, <html>.

[STRIKEOUT:This is strikeout.]

Superscripts: a\ :sup:`bc`\ d a\ :sup:`hello` a\ :sup:`hello there`.

Subscripts: H\ :sub:`2`\ O, H\ :sub:`23`\ O, H\ :sub:`many of them`\ O.

These should not be superscripts or subscripts, because of the unescaped
spaces: a^b c^d, a~b c~d.

Smart quotes, ellipses, dashes
==============================

“Hello,” said the spider. “‘Shelob’ is my name.”

‘A’, ‘B’, and ‘C’ are letters.

‘Oak,’ ‘elm,’ and ‘beech’ are names of trees. So is ‘pine.’

‘He said, “I want to go.”’ Were you alive in the 70’s?

Here is some quoted ‘code’ and a “quoted link
<http://example.com/?foo=1&bar=2>__”.

Some dashes: one—two — three—four — five.

Dashes between numbers: 5–7, 255–66, 1987–1999.

Ellipses…and…and….

LaTeX
=====

-  
-  :math:`2 + 2 = 4`

-  :math:`x \in y`

-  :math:`\alpha \land \omega`

-  :math:`223`

-  :math:`p`-Tree

-  Here’s some display math:

   :math:`\frac{d}{dx}f(x) = \text{lcsub}h \rightarrow 0\frac{f(x + h) - f(x)}{h}`

-  Here’s one that has a line break in it:
   :math:`\alpha + \omega \times x^{2}`.

These shouldn’t be math:

-  To get the famous equation, write $e = mc^2$.

-  $22,000 is a *lot* of money. So is $34,000. (It worked if “lot” is
   emphasized.)

-  Shoes ($20) and socks ($5).

-  Escaped $: $73 *this should be emphasized* 23$.

Here’s a LaTeX table:

Special Characters
==================

Here is some unicode:

-  I hat: Î

-  o umlaut: ö

-  section: §

-  set membership: ∈

-  copyright: ©

AT&T has an ampersand in their name.

AT&T is another way to write it.

This & that.

4 < 5.

6 > 5.

Backslash: \\

Backtick: \`

Asterisk: \*

Underscore: \_

Left brace: {

Right brace: }

Left bracket: [

Right bracket: ]

Left paren: (

Right paren: )

Greater-than: >

Hash: #

Period: .

Bang: !

Plus: +

Minus: -

13. .. rubric:: Links
       :name: links

    9. .. rubric:: Explicit
          :name: explicit

Just a `URL <file:///url/>`__.

`URL and title <file:///url/>`__.

`URL and title <file:///url/>`__.

`URL and title <file:///url/>`__.

`URL and title <file:///url/>`__

`URL and title <file:///url/>`__

`with_underscore <file:///url/with_underscore>`__

`Email link <mailto:nobody@nowhere.net>`__

Empty.

Reference
---------

Foo `bar <file:///url/>`__.

With `embedded [brackets] <file:///url/>`__.

`b <file:///url/>`__ by itself should be a link.

Indented `once <file:///url>`__.

Indented `twice <file:///url>`__.

Indented `thrice <file:///url>`__.

This should [not][] be a link.

[not]: /url

Foo `bar <file:///url/>`__.

Foo `biz <file:///url/>`__.

With ampersands
---------------

Here’s a link with an ampersand in the URL
<http://example.com/?foo=1&bar=2>__.

Here’s a link with an amersand in the link text:
`AT&T <http://att.com/>`__.

Here’s an `inline link <file:///script%3Ffoo=1&bar=2>`__.

Here’s an `inline link in pointy
braces <file:///script%3Ffoo=1&bar=2>`__.

Autolinks
---------

With an ampersand: http://example.com/?foo=1&bar=2

-  In a list?

-  http://example.com/

-  It should.

An e-mail address: nobody@nowhere.net

   Blockquoted: http://example.com/

Auto-links should not occur here: <http://example.com/>

or here: <http://example.com/>

Images
======

From “Voyage dans la Lune” by Georges Melies (1902):

|image0|

lalune

Here is a movie |image1| icon.

Footnotes
=========

Here is a footnote reference, [1]_ and another. [2]_ This should *not*
be a footnote reference, because it contains a space.[^my note] Here is
an inline note. [3]_

   Notes can go in quotes. [4]_

1. And in list items. [5]_

This paragraph should not be part of the note, as it is not indented.

.. [1]
   Here is the footnote. It can go anywhere after the footnote
   reference. It need not be placed at the end of the document.

.. [2]
   Here’s the long note. This one contains multiple blocks.

   Subsequent blocks are indented to show that they belong to the
   footnote (as with list items).

   { <code> }

   If you want, you can indent every line, but you can also be lazy and
   just indent the first line of each block.

.. [3]
   This is *easier* to type. Inline notes may contain
   `links <http://google.com/>`__ and ] verbatim characters, as well as
   [bracketed text].

.. [4]
   In quote.

.. [5]
   In list.

.. |image0| image:: media/image1.jpeg
   :width: 2.08333in
   :height: 2.08333in
.. |image1| image:: media/image2.jpeg
   :width: 0.27778in
   :height: 0.30556in
