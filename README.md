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

## General Update Pattern
1. Grab the update selection make any changes unique to that selection and store the selection in a video
2. Grab the exit selection and remove any unnecessary elements
3. Grab the enter selection and make any changes unique to that selection
4. merge the enter and update selections, and make any changes that you want to be shared across both the selections

eg:
``` javascript
var addAll = d3.select('#addAll');
addAll.on('click', function(){
  quotes = quotes.concat(newQuotes);

  var listItems = d3.select('#quotes').selectAll('li').data(quotes);
  listItems
      .enter()
      .append('li')
      .text(d => '"' + d.quote + '" - ' + d.movie + ' (' + d.year + ')')
      .style("margin", "20px")
      .style("font-size", d => d.quote.length < 25 ? "2em" : "1em")
      .style("background-color", d => colors[d.rating])
      .style("border-radius", "8px")
      .merge(listItems)
      .style('color','#0000ff')
      .style("padding", "10px")
});

```

