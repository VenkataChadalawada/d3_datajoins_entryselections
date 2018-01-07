# d3_datajoins_entryselections

You can take a look on demo here - https://jsfiddle.net/Venkata_Chadalawada/jmctoLeo/

Notes:

Q1)How many keys will the following D3 selection have?
d3.selectAll("p")
Ans: 2
The keys will be _parents and _groups.

Q2)How many keys will the following D3 selection have?
d3.selectAll("p").data([1,2,3])
Ans: 4
The keys will be _groups, _parents, _enter, and _exit.

Q3)What will be the parent node in the following selection?
d3.select("body").selectAll("p")
Ans: body

Q4) What will be the parent node in the following selection?
d3.selectAll("p")
Ans: html
This is the default parent for a D3 selection.

Q5) When you pass a callback into a selection method like .text , .style , or .on , what does the first argument in the callback function represent?
Ans: data joined to current element


Q6) By default, how does D3 join elements and data together when you use the data method?
Ans:The first element in the selection is matched with the first piece of data, the second element in the selection is matched with the second piece of data, and so on.

Q7)What does the second argument in the data function allow you to do?

Ans: It lets you to define a key function to specify how elements & data should be joined together
