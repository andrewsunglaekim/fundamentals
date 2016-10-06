**WDI Fundamentals Unit 5**

---

##![Your Turn](../assets/exercise.png) Your Turn

### Elk Web Design: Part 3

This is final part of the ELK Design! We'll become more familiar with positing elements and images. We'll be dealing with floats. Remember, floats pull whatever element they're applied to out of the normal document flow. They're your secret weapon for positioning HTML elements on a page!

### Instructions

Here's the editor you should use to write your code. You'll first need to copy over your code from the previous ELK exercise into the editor. As usual, **don't forget to fork and save your JSBin link.**

<a class="jsbin-embed" href="http://jsbin.com/tifivo/embed?html,css,outputheight=600px">JS Bin on jsbin.com</a><script src="http://static.jsbin.com/js/embed.min.js?3.35.12"></script>

When you have your code from your previous exercise, follow the instructions below.

1 . Set your div's font-size to 1.2em, and tell it to only stretch across 50% of the screen's width.

2 . Tell both divs to display as inline-block elements.

3 . Add an `id` attribute to the divs. Use `about` for the first and `services` for the second.

4 . Create CSS rules (selectors) for `#about` and `#services`.

5 . Give `#about` a float of left.

6 . Give `#services` a float of right.

At this point, you'll notice that some things are not so awesome here.
  * The two columns are smushed together.
  * The footer is behaving oddly.

7 . Let's start with the quickest fix. Give the footer a clear value of both.

8 . The footer's in the right place, but the two columns are still too close! What do you know about adding whitespace between HTML elements? Currently, #services and #about are 50% of the page width each. Here's some math. You're borrowing from the page's width to add a 2% padding on all four sides, so that each div keeps its total width of 50%. So go ahead and add a width of 46% and padding of 2%.

Fabulous!

9 . Now let's box up and position the four listed services in the right-hand column.

  * Create an li rule, and give it a float property with a value of left.
  * Set its width to 50% and its height to 6em.

10 . Give li an outline value of `3px solid #222222`.

11 . Set its text-align to center, and line-height to 6em.

*Well done! The basics of the multicolumn layout are all laid out. All that's left to finish are some visual elements, including color.*

12 . Assign img a width of 480px.

13 . Flip to your HTML, and wrap a new div, called "hero", around the main image.

*Your img might freak out. Don't worry. It's because the "hero" div is grabbing the default div style written for your columns. Let's prevent that from happening. You need to counteract the div's width, margin, and display values.*

14 . In your HTML, wrap a section around both divs: open it after the `</header>` closing tag, and close it before the opening `<footer>` tag.

15 . Create a CSS style for the section. Set its background to `#222222`, and make its color white. Make the section's overflow:auto.

16 . Set the h2 color to pale yellow: #fffebb. Set h2's border-bottom-color to #fffebb as well.

17 . Set the li color to black, and its background to white.

Bravo! Well done. Don't forget to save your code in JSBin so you can come back to it and ask your instructors any questions you might have!

[Take the Quiz for Unit 5 now!](10_quiz.md)
