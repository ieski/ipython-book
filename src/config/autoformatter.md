# TerminalInteractiveShell.autoformatter

<pre class="output">
## Autoformatter to reformat Terminal code. Can be `'black'` or `None`
#  Default: None
</pre>

`black` is [the uncompromising Python code formatter](https://github.com/psf/black). It can make collaboration on a project consistent— no matter the style of the coder, `black` will format the code to its specifications, so everything is nice and tidy.

```
c.TerminalInteractiveShell.autoformatter = 'black'
```

Enabling this can turn something like this:

<pre class="output">
In [1]: prices = {
   ...: 'apple': 0.40, 'banana': 0.50
   ...: }
   ...: my_purchase = {
   ...:     'apple': 1,
   ...:     'banana': 6}
   ...: grocery_bill = sum(
   ...: prices[fruit] * my_purchase[fruit]
   ...:                    for fruit in my_purchase
   ...:                    )
   ...: print('I owe the grocer $%.2f' % grocery_bill)
I owe the grocer $3.40
</pre>

…into this:

<pre class="output">
In [1]: prices = {"apple": 0.40, "banana": 0.50}
   ...: my_purchase = {"apple": 1, "banana": 6}
   ...: grocery_bill = sum(prices[fruit] * my_purchase[fruit] for fruit in my_purchase)
   ...: print("I owe the grocer $%.2f" % grocery_bill)
I owe the grocer $3.40
</pre>

It's very handy for cleaning up your code style, especially if the project you're working on uses `black`. In order for this to work, you need to have `black` installed in your environment:

```
pip install black
```