# Plus Minus Code

```
arr = [1, 1, 0, -1, -1]

let positive = 0,
    negative = 0,
    zero = 0
    
for(let i of arr) {
    i > 0 ? positive++ : i < 0 ? negative++ : zero++
}

console.log((positive / arr.length).toFixed(6))
console.log((negative / arr.length).toPrecision(6))
console.log((zero / arr.length).toPrecision(6))
```

# Plus Minus Code

```
arr = [1, 1, 0, -1, -1]
```
// define mutable variables we can add to as we iterate over our array
```
let positive = 0,
    negative = 0,
    zero = 0
```

// iterate over each item in the array and do the following: if item is greater than 0, add 1 to positive; if item is less than 0, add 1 to negative; if item is equal to 0, add 1 to zero

```
for(let i of arr) {
  i > 0 ? positive++ : i < 0 ? negative++ : zero++
}
```

// divide the sums of each variable by the length of the array to find the ratio, then use the toFixed() method to show six decimals

```
console.log((positive / arr.length).toFixed(6))
console.log((negative / arr.length).toPrecision(6))
console.log((zero / arr.length).toPrecision(6))
```

=======================
=======================
=======================
=======================

# Time Conversion Code

```
function timeConversion(s) {
	let hour = s.slice(0,2);
	let minutes = s.slice(3,8)

	if(s[8] === 'A') {
		if(hour === '12') {
			return '00' + ':' + minutes
		} else {
			return hour + ':' + minutes
		}
	}

	if(s[8] === 'P') {
		if(hour === '12') {
			return hour + ':' + minutes
		} else {
			return (parseInt(hour) + 12).toString() + ':' + minutes
		}
	}
}

timeConversion('09:01:00AM')
```

# Time Conversion Code Explaination
There are a few things that immediately stick out to me:
1) Each time string has the same length
2) The 8th index in the string will be either A or P, which will dictate whether we add to the hour (PM times) number or not (AM times).
3) AM times, with the exception of midnight, have nothing added to them (1AM = 1)
4) PM times, with the exception of noon, have 12 added to them (1PM = 13)

We’ll need a couple of conditional statements that take what we said above in mind so that we’re doing the correct math depending on AM or PM.

```
function timeConversion(s) {
```
// the only part of the time that will change is the hour, so create a variable that stores only the hour part of the time
```	
	let hour = s.slice(0,2);
```	

// we’re not going to be changing the minutes and seconds, but we’ll still need to add them our new hour in order to show the entire time, so create a variable that stores only the minutes and seconds part of the time
```
	let minutes = s.slice(3,8)
```
	
// if the 8th index in the time is ‘A’, we will be dealing with AM time
```	
	if(s[8] === 'A') {
```
// if the hour is 12 (midnight), replace 12 in the time with 00 and then concatenate the minutes variable
// make sure to include a colon between the hour and minutes so your time string is correctly displayed
```		
		if(hour === '12') {
			return '00' + ':' + minutes
```
// if the hour isn’t 12, no adding to the hour is needed so just return the hour and then concatenate the minutes variable
// make sure to include a colon between the hour and minutes so your time string is correctly displayed
```
		} else {
			return hour + ':' + minutes
		}
	}
```
// if the 8th index in the time is ‘P’, we will be dealing with PM time
```
	if(s[8] === 'P') {
```
// if the hour is 12 (none), no adding to the hour is needed so just return the hour and then concatenate the minutes variable
// make sure to include a colon between the hour and minutes so your time string is correctly displayed
```
		if(hour === '12') {
			return hour + ':' + minutes
```
// if the hour isn’t 12, add 12 to the hour and then concatenate the minutes variable
// make sure to include a colon between the hour and minutes so your time string is correctly displayed
```
		} else {
			return (parseInt(hour) + 12).toString() + ':' + minutes
		}
	}
}
```
// invoke the function to test the time is being converted correctly
```
timeConversion('09:01:00AM')
```

=======================
=======================
=======================
=======================
