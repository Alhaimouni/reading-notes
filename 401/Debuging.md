## What are the types of errors i could see ?!


#### ReferenceError: 
  Happens if you call a variable,function,object...etc and Misspelled the name of it 
<pre>Transposed, missing, or mis-capitalized characters in a variable or function name
will have the browser looking for an object that doesn't exist - and complain in the form of a reference error.
JavaScript variable and function names are case-sensitive.</pre>

#### SyntaxError:
<ul>
  <li>Catch Unclosed Parentheses, Brackets, Braces and Quotes </li>
  <li>Catch Mixed Usage of Single and Double Quotes </li>
</ul>
  
#### HiddenErrors(Logical):
 
<ul>
  <li>Catch Use of Assignment Operator Instead of Equality Operator</li>
  <li>Catch Missing Open and Closing Parenthesis After a Function Call </li>
  <li>Catch Arguments Passed in the Wrong Order When Calling a Function</li>
  <li>Catch Off By One Errors When Using Indexing</li>
</ul>
<pre>Off by one errors (sometimes called OBOE) crop up when you're trying to target a specific index of a string or array (to slice or access a segment),
or when looping over the indices of them. JavaScript indexing starts at zero, not one,
which means the last index is always one less than the length of the item. If you try to access an index equal to the length,
the program may throw an "index out of range" reference error or print undefined.</pre>
