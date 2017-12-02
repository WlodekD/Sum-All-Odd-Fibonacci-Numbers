# Sum-All-Odd-Fibonacci-Numbers
Given a positive integer num, return the sum of all odd Fibonacci numbers that are less than or equal to num.  The first two numbers in the Fibonacci sequence are 1 and 1. Every additional number in the sequence is the sum of the two previous numbers. The first six numbers of the Fibonacci sequence are 1, 1, 2, 3, 5 and 8.  For example, sumFibs(10) should return 10 because all odd Fibonacci numbers less than 10 are 1, 1, 3, and 5.


function sumFibs(num) {

  var arr = [1];
  var odds = [];
  
  for(var i=1; i<=num;){
    arr.push(i);
    i = arr[arr.length - 1]+arr[arr.length - 2];
  }
  
  for(var j=0; j<arr.length; j++){
    if(arr[j] % 2 != 0){
      odds[j] = arr[j];
    }
  }
  
  function filtered(odds){
    return odds != null;
  }
  odds = odds.filter(filtered);
  
  var result = 0;
  for(var k in odds){result += odds[k];}
  
  return result;
}

sumFibs(9);
