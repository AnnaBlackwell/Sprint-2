Nice comments on Agile. We'll see if you like it in practice. :-)

Superb work on color contrasts! Best response so far. Nice.

Colors look good, too (even if you can't spell color ;-). Or am I the one can't spell it? Almost looks like ASCII art.

HTML nice! Clever use of the `<aside>` element. Love it.

One style issue. Please don't use word wrap and long lines. If an element exceeds 80 characters in length (including indent), then please break it up into multiple lines. I know you can't always keep HTML under 80 characters, but try to get close. And with JavaScript, no exceptions! Under 80 characters all the time.

So this:

```html
<p>The HTML Article Element (&lt;article&gt;) represents a self-contained composition in a document, page, application, or site, which is intended to be independently distributable or reusable (e.g., in syndication). This could be a forum post, a magazine or newspaper article, a blog entry, an object, or any other independent item of content. Each &lt;article&gt; should be identified, typically by including a heading (h1-h6 element) as a child of the &lt;article&gt; element.</p>
```

Becomes this:

```html
<p>
  The HTML Article Element (&lt;article&gt;) represents a self-contained
  composition in a document, page, application, or site, which is intended to be
  independently distributable or reusable (e.g., in syndication). This could be
  a forum post, a magazine or newspaper article, a blog entry, an object, or any
  other independent item of content. Each &lt;article&gt; should be identified,
  typically by including a heading (h1-h6 element) as a child of the
  &lt;article&gt; element.
</p>
```

It's just easier to read. Yeah, I know. Eventually, this will all be automated and then it will look messy. But if it's under your control, then make it a habit to keep it as clean and neat as possible. It will make your code look more elegant, make it easier to read and easier to debug, and it will make your instructors happy. :-)

Good responses on the pair programming. No worries! The assignments will get increasingly difficult and you'll be pairing every day on site.

The JS looks good. I see you copied and pasted from the REPL. That's great that you're using the REPL, but it will be easier for us if you go the other direction. Write your code in a file and then paste it into the REPL. Then you have clean code in your file.

Also, we'll be following the [standard.js]() style guide. So we're gonna need a bit more space!

This:

```js
function avg (x, y) {
... return (x+y)/2
... }
> avg (6, 7)
6.5


function aveofthree (x, y, z) {
... return (x+y+z)/3
... }

> aveofthree (3, 8, 4)
5

function isodd (x) {
... return (x%2)
... }

> isodd (4)
0
> isodd (7)
1
```

Should look like this:

```js
function avg (x, y) {
  return (x + y) / 2
}

function avgOfThree (x, y, z) {
  return (x + y + z) / 3
}

function isOdd (x) {
  return (x % 2)
}
```

Note that function names are camelCase in JavaScript. Be consistent. If you have an `avg` function, then your `avgOfThree` should use a g, too, not `aveOfThree`.

Start practicing now! Then if you want to show output, this is the best practice:

```js
avg(6, 7)           // returns 6.5
avgOfThree(3, 8, 4) // returns 5
isOdd(4)            // returns 0
isOdd(7)            // returns 7
```

I had the `isOdd` function return 1 or 0 to make it easier. Then most of your cohort made it more difficult! Congratulations for getting that one right! But note that normally a function with a name starting with `is` will return a boolean, not a number. We can convert our number to a boolean in a couple of ways. The first is the most obvious: with a `===` operator:

```js
function isOdd (x) {
  return x % 2 ===  1
}
```

Obviously, if we used `=== 0` we'd have to call the function `isEven`, right? The other way is a neat cheat. We can take advantage of the fact that in JavaScript, 1 is considered "truthy" and 0 is considered "falsy", which means that they evaluate to `true` and `false` respectively even though technically they're not.

To convert to a real boolean, we can use the `!` (not) operator. This converts truthy to `false` and falsy to `true`. But that's the opposite of what we want! So let's use it *again* to convert back again. That means that `!!` converts a "truthy" value to `true` (the boolean) and a "falsy" value to `false`.

```js
function isOdd (x) {
  return !!(x % 2)
}
```

Should you do this? Probably not. It's much less obvious and readable. But you will see it out in the wild, so good to know how it works.

Questions?

Excellent work on the accessibility and usability deliverables. Hope you're finding that stuff interesting. And excellent work all around. Thank you and keep it up!

