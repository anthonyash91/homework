<code>
  arr = [1,3,5,-4,-9,-6,-1,0,0]
let positive = 0
let negative = 0
let zero = 0

for(let i = 0; i < arr.length; i++) {
  if(arr[i] > 0){
    positive += 1
  }  else if(arr[i] < 0){
    negative += 1
  } else if(arr[i] === 0){
    zero += 1
  }
}

const positiveRatio = positive / arr.length
const negativeRatio = negative / arr.length
const zeroRatio = zero / arr.length

console.log(positiveRatio.toFixed(6))
console.log(negativeRatio.toPrecision(6))
console.log(zeroRatio.toPrecision(6))
                         </code>
