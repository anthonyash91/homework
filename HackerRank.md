## Plus Minus Code With Explaination
<pre><code>arr = [1,1,0,-1,-1]</code></pre>

// define mutable variables we can add to as we iterate over our array
<pre><code>let positive = 0,
    negative = 0,
    zero = 0</code></pre>

// iterate over each item in the array and do the following: if item is greater than 0, add 1 to positive; if item is less than 0, add 1 to negative; if item is equal to 0, add 1 to zero
<pre><code>for(let i of arr) {
  i > 0 ? positive++ : i < 0 ? negative++ : zero++
}</code></pre>

// divide the sums of each variable by the length of the array to find the ratio, then use the toFixed() method to show six decimals
<pre><code>console.log((positive / arr.length).toFixed(6))
console.log((negative / arr.length).toPrecision(6))
console.log((zero / arr.length).toPrecision(6))</code></pre>

