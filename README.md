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
