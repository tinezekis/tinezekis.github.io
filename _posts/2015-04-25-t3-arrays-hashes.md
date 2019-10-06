---
layout: post
title: "Technical Blog | Arrays & Hashes"
post_title: "Keeping Track of It All"
post_subtitle: "Arrays, Hashes, and When to Use Them"
date: 2015-04-25
categories: blog technical
---

<p>
  In all programming languages, we can assign values to variables. For instance, if I want to create a sting that I will use multiple times and/or manipulate in some way, I will want to name it. In Ruby, we assign variables by listing the name followed by an equal sign and the assigned value. For example, <code>greeting = 'Hello, loyal blog readers!'</code> would tell the program that the variable <code>greeting</code> points to the string <code>'Hello, loyal blog readers!'</code> So any time I wanted to use the string or call some method on it, I can use <code>greeting</code> as a sort of nickname. We can also assign other types of values like integers or floats (numbers with a decimal point). For instance, <code>example_int = -47</code> assigns the integer value -47 to the variable <code>example_int</code>. Now, if I call the absolute value method thusly, <code>example_int.abs</code>, the return will be the absolute value of the variable (47).
</p>
<p>
  So we have a way to store values into our variables. But what if we have a lot of variables we need to keep track of. For instance, what if I wanted to store a list of responses to a single question by many respondents, or an entire grocery list? I might not want to create and assign variables for each of these items, as this could become quite cumbersome (<code>response1 = 3</code>, <code>response2 = 7</code>, ..., <code>response 36 = 9</code>). This is where we might choose to use something called an <b>array</b>. Arrays store a list of variables into a series of slots, or indices. So I could create just one array for my entire list of responses: <code>responses = [3, 7,..., 9]</code>. Then, I can reference each item within the list based on its index (slot) in the array. But here's where things get tricky: we actually begin counting from index 0. Thus, <code>responses[0]</code> refers to the first index and returns a value of 3. In order to get our second and 36th values, we would need to call <code>responses[1]</code> and <code>responses[35]</code>, respectively. If our list has 36 items, then the 37th index (<code>responses[36]</code>) would return the <code>nil</code> value, or "nothing". There can even be indices within a list that return the <code>nil</code> value. In order to understand this better, let's talk about another way we can assign values to an array.
</p>
<p>
  Rather than listing all values at once, we can also assign values to an array individually by index, or slot position. For instance, I can create an empty array like this: <code>chicago_teams[]</code> or <code>chicago_teams = Array.new</code> (please note that "Array" gets capitalized in this second option). Then, I can assign individual values thusly:<br>
  <code>chicago_teams[0] = 'Bulls'</code><br>
  <code>chicago_teams[1] = 'White Sox'</code><br>
  <code>chicago_teams[3] = 'Blackhawks'</code><br>
  <code>puts chicago_teams</code><br>
  Printing out the array would produce the following:<br>
  <code>Bulls</code><br>
  <code>White Sox</code><br>
  <code>nil</code><br>
  <code>Blackhawks</code><br>
  The third index (<code>chicago_teams[2]</code>) has not been assigned and thus contains the <code>nil</code> value.
</p>
<p>
  Hopefully by now, we're getting used to referring to items in an array by their index numbers. But what if we don't want to reference our items this way? For example, what if we had a list of all basketball teams in the NBA? Would we really want to remember which index number went with each team? Wouldn't it be easier to reference those teams by city instead? Well, fortunately, we have a tool for that as well: a <b>hash</b>. A hash organizes information in key-value pairs. So in this case, we might reference the value <code>'Bulls'</code> with the key <code>chicago</code> and <code>'Bucks'</code> with the key <code>milwaukee</code>. We could use any of these formats to set up the hash:<br>
  <code>nba_teams = {'chicago', 'Bulls', 'milwauke', 'Bucks'}</code><br>
  <code>nba_teams = { ['chicago', 'Bulls'], ['milwaukee', 'Bucks'] }</code><br>
  <code>nba_teams = {'chicago' => 'Bulls', 'milwaukee' => 'Bucks'}</code><br>
  Or, just like with the array, we can create an empty hash and then assign key-value pairs later:<br>
  <code>nba_teams{}</code> or <code>nba_teams = Hash.new</code> (notice that "Hash" also gets capitalized in this situation)<br>
  <code>nba_teams['chicago'] = 'Bulls'</code><br>
  <code>nba_teams['milwaukee'] = 'Bucks'</code><br>
  No matter how we created and assigned the hash, we can now reference the values by their keys. So <code>nba_teams['chicago']</code> now points to the value of string <code>'Bulls'</code>.
</p>
<p>
  So we can see that hashes and arrays have different properties that make them useful for different situations. Arrays help us to keep track of a list of values that have a specific order. We can use array commands to rearrange this order, sort the items in the list, reference items by index number, and many other tasks. All the while, the array keeps track of where each item is stored. Hashes do not maintain information in a particular order. Instead, values are stored and referenced by their keys. Perhaps we want to keep track of Sally and Joe's respective responses to a question, instead of respondents 1 and 2. In this case, a hash might be a more useful way to store this information. In order to determine whether you need an array or a hash, it will be best to consider what you need to do with this information, and how it can most conveniently be referenced when needed.
</p>
<p>
  I hope this brief introduction has given you an idea of how these two objects differ and when you might need either one. Stay tuned for more of my coding discoveries as the journey continues!
</p>
