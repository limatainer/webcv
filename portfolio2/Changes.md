When you first ran the code from wk1 branch you saw in the logs some issues with font imports here is a breakdown and the fix for wk2:

The @import statement must
come at the very beginning of the CSS file, before any other rules (except
@charset or empty @layer).
I moved the Google Fonts @import statement to line 2, right after
the Tailwind import and before all the @font-face rules.
The error occurred because CSS requires all @import statements to appear at
the beginning of the file, before any other CSS rules. Now both imports
are at the top of portfolio1/src/style.css:1-2, which should resolve the
build error.
The Google Fonts @import on line 21 comes after the
@font-face rules, but all @import statements must come at the very
beginning of the CSS file.
The problem is that when Vite processes @import
'tailwindcss';, it expands all of Tailwind's CSS, and then the Google Fonts
@import appears after that expanded content, which causes the error.
The best solution is to load the Google Fonts in the HTML file instead.

1. Added Google Fonts to the HTML (portfolio1/index.html:7-9) - This is the
   recommended way to load external fonts with Vite/Tailwind, as it avoids
   the @import ordering issues
2. Removed the problematic @import from the CSS file
   (portfolio1/src/style.css:1-3)
   The issue was that when Vite processes @import 'tailwindcss', it expands
   all of Tailwind's CSS first, and then any subsequent @import statements
   appear after that expanded content, violating CSS rules that require all
   imports at the beginning.
   Loading the font via <link> tags in the HTML is also better for
   performance. The error should now be resolved!

---

After creating a page inside Home I have also created not so good practice can you tell?
