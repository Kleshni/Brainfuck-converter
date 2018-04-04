Text to Brainfuck converter
===========================

Generates a Brainfuck programm printing the desired text.

Use it [online](https://kleshni.github.io/Brainfuck-converter/).

Comparing it with [another](https://copy.sh/brainfuck/text.html) converter by generated programms for Shakespeare's [Sonnet 1](Sonnet%201.txt):

|                   | This algorithm | Copy's algorithm |
| ----------------- | -------------- | ---------------- |
| Code size         | 4827           | 6514             |
| Executed commands | 121493         | 182140           |
| Consumed memory   | 1856           | 331              |

The implemented algorithm:

```python
result = ">--->--->--->"

for i in reversed(text):
	for j in range(3):
		result += ["---", "--", "-", "", "+", "++", "+++"][i % 7] + ">"
		i //= 7

result += "+[<+++[-<+++++++>]<+++[-<+++++++>]<+++[.>]<]"
```

Links
-----

* [Source code](https://github.com/Kleshni/Brainfuck-converter/archive/master.zip).
* [Git repository](https://github.com/Kleshni/Brainfuck-converter.git).
* [Issue tracker](https://github.com/Kleshni/Brainfuck-converter/issues).
* Bitmessage: BM-2cT5WWccBgLsHTw5ADLcodTz4dbqdtrwrQ.
* Mail: [kleshni@protonmail.ch](mailto:kleshni@protonmail.ch).
