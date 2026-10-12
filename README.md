Calculator
==========

A small calculator I built with plain HTML, CSS and JavaScript. One file, nothing
to install, no libraries, no build step.

Files
-----
calculator.html    the whole thing (html, css and js all in one file)
README.md          this

How to run it
-------------
Double click calculator.html. It opens in the browser and just works.

If you use VS Code you can also right click it and pick "Open with Live Server".
Same result, only it auto reloads when you edit the file.

What the buttons do
-------------------
C           clears the display
backspace   deletes the last character you typed (the orange erase button)
%           modulo, so 7 % 6 gives 1
/ x - +     divide, multiply, subtract, add
.           decimal point
=           shows the answer

The x button is multiply. On the keyboard use * for that, both work.

Keyboard
--------
0-9 and .       numbers
+ - * /         operators
Enter or =      show the answer
Backspace       delete last character
c               clear

How the math works
------------------
It collects everything into one expression, swaps x for * and runs it through
eval(). eval is fine here since only digits and operators can get in, but I would
not copy that into a real project. Because it uses normal JS math it follows the
usual order, so 2 + 3 x 4 comes out as 14, not 20.

Things to know
--------------
- dividing by zero shows Error, that's on purpose
- if you press two operators in a row the last one wins, so 7 + x 6 becomes 7 x 6
- after pressing =, typing a number starts fresh but pressing an operator
  continues from the answer
- you can't put two dots in the same number
- long decimals show as is, so 0.1 + 0.2 = 0.30000000000000004

Not done
--------
- no history
- no memory keys
- the % button does modulo, not the "percent of" thing phones do
