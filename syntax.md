## if you want to remove the value from list
**list.remove(Integer.valueOf(arr[i])**
## If you want to filter special characters in java, use
  **Character.isLetterOrDigit(char)**
## In map, use this syntax,
 **map.put(a,map.getOrDefault(a,0)+1)**
## How to get n- digit numbers in java ##
**int start=(int)Math.pow(10,n-1);**

**int end=(int)(Math.pow(10,n)-1);**
## How to convert a number into Binary String ##
**String Binary=Integer.toBinaryString(number)   ---TimeComplexity-O(logn) SpaceComplexity-O(logn)**
## n-digit binary Number
**int start=0;
int end=(int)Math.pow(2,n)-1;**
## Convert int to string
**Integer.toString(num)**
## Convert String to int
**Integer.Valueof() OR Integer.parseInt()**
## Sum of n numbers 
**n(n+1)/2**
## sum of n numbers square 
**n(n+1)(2n+1)/6 ;**
## for n digit number
**even count=(n+1)/2 , oddCount=n/2**
## sb.RemoveCharAt(i);
## Sudoko solver 3*3 box checking
**if(board[3*(row/3)+i/3][3*(col/3)+i%3]==c);**
## if return type is long , but my ans is longer than long , MOD=10^9+7, return ans%MOD
## Heap
**PriorityQueue<int[]> minHeap=new PriorityQueue<>((a,b)->
{if(a[1]!=b[1]) return Integer.compare(b[1],a[1]);

else return Integer.Compare(a[0],b[0]);
} );**



