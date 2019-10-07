---
layout: post
title: "Enumerable#map"
subtitle: "Taking It One Element at a Time"
date: 2015-05-03
categories: blog technical
---

<h4>Assignment: Technical Blog | Enumerable Methods</h4>

<p>
  In Ruby, <code>Enumerable</code> is a module that allows us to access each element out of a collection, one at a time. It is used as a mix-in for various classes that contain multiple elements, such as <code>Array</code>s, <code>Hash</code>es, and <code>Range</code>s. If we think of enumerable as an adjective, then <code>Enumerator</code> is the noun form. It is a method object (a noun that performs a verb), a tool we can use to <i>enumerate</i> an action, one at a time, on every element of another object. For now, we will focus on one such enumerator: the <code>map</code> method.
</p>
<p>
  <code>Enumerable#map</code> is an enumerator that returns a new array in which each index is the result of performing the block one time on each element in a collection. For example:
  <pre><code>(1..5).map { |i| i * i }</code></pre>
  <pre><samp>=> [1, 4, 9, 16, 25]</samp></pre>
  The block (in curly brackets) directed this <code>map</code> method to take each element of the range 1 - 5 (inclusive) and multiply the element by itself. The result is an array containing a list of the first five perfect squares. It is important to note, however, that if the action in the block does not have a return value, the array created will have a <code>nil</code> value in each index. For example, the <code>print</code> method will print a string to the console, but does not return any value. So, if we wanted to print each element in our range with a space in between, we might do so thusly:
  <pre><code>(1..5).map { |i| print i.to_s + ' ' }</code></pre>
  <pre><samp>=> 1 2 3 4 5 => [nil, nil, nil, nil, nil]</samp></pre>
  Let's talk a little bit about what went on here. The block instructs our <code>map</code> method to take each element in the range and print that element (converted to a string) and add a space afterward. The <code>print</code> method does not create a line break, so each of our elements (as well as the next line in the terminal) all get printed to one line. The next piece is the array that got returned. Each time we printed an element, the <code>nil</code> value was returned in our array. This is why we see <code>nil</code> five times, one for each element of the range.
</p>
<p>
  It is also important to note that if no block is given, the return is an enumerator object. For example:
  <pre><code>(1..5).map</code></pre>
  <pre><samp>=> &lt;Enumerator: 1..5:map&gt;</samp></pre>
  Thus, we can later determine what this enumerator will do. For example, we will create an enumerator called <code>enum</code>:
  <pre><code>enum = (1..5).map</code></pre>
  <pre><samp>=> &lt;Enumerator: 1..5:map&gt;</samp></pre>
  <pre><code>example.map { |i| i + 1 }</code></pre>
  <pre><samp>=> [2, 3, 4, 5, 6]</samp></pre>
  After the enumerator was created, we are able to apply the <code>map</code> block with new content. In this case, we added 1 to each element.
</p>
<p>
  Well, this has been just a small look into one thing that enumerators can do. I hope it has piqued your interest and that you will investigate enumerator methods further, as I will. Please check in again as I continue my journey into web development. I will continue to post about my learnings along the way. And, for your sake and mine, I'm going to resist the map pun here. Until next time, happy coding!
</p>
