## 9th March 2023

I forgot almost most of the topics of c++ i learned back in the days, planning to revise all of those once again.
What I remembered today while solving atcoder contest problem is that the function pow(a,b) = $a^b$.
When I am outputting a direct computational result which is larger than $1*10^9$, I should at first store it in a long int variable then output the result. For example, instead of doing this ``` cout<<pow(9,9); ```, I should store the value of pow(9,9) in a long int variable then output it. 
There is a couple of ways to convert int to character which can be found in geekforgeeks. I am comfused of the fact that whether I have to know all of them or not, or which method is the most efficient one. Most simpler one that I found is ```char(65);```
I should have a rough idea of the ascii codes/ascii table. I should know that 48 represents '0' and 57 represents '9' as a char, 65 represents 'A' and 90 represents 'Z' as a char, and 97 represents 'a' and 122 represents 'z' as a char.

## 14th March 2023

This is a special day. It's a pi day! Hurray! 
Onething that I learnt today is that that I should always considering while solving any problems in CP, whether I am acessing an out of range value of an array, specially in loops (for/while). I should always consider what are the else case of a conditional statement; I always forget about that. Next time, I should be careful about it. 
The scientific notation of writing 1*10^7 would be 1e7

## 15th March 2023
I can use this piece of code as a short form/an efficient way to input an array of numbers: ```for(int i = 0;i<5*n ;i++)cin>>arr[i];```, but i have to keep in mind that only one line ending with one semicolon will be executed, which means this ```for(int i = 0;i<5*n ;i++)cin>>arr[i];sum+= arr[i];``` will not work.

One way of sorting an array is to use ```sort(arr, arr + n);```, I literally forgot about it for a long time.

One way of fixing the number of decimal numbers in output is to use ```cout<<fixed<<setprecision(5)<<n;```
