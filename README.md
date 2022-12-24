# cpp-commands
These are the C++ concepts which I might need in future 

 # Some beginnaer Tricks #
 
 ### Operators ###
 ```C++
 != 3    x = x|3  >>= 3  x= x>>3    <<= 3  x= x<<3
 ```
 
 ### Concatenation ###
 ```C++
 Concatenation "+"
 .append()
 firstname = "Mubin";
 lastname = "Hasan";
 firstname.append(lastname);
 ```
 ### Some other tricks ###
 ```C++
 cout<< (10>9); // Output true 1 //
 cout<< (9>10); // Output false 0 //
 ```
 
 ```C++
 for(int i=0; i<10; i++){
 if (i==4){break;} // Jumps out of the loop //
 else {cout << i} }
```

```C++
for(int i=0; i<10; i++){
 if (i==4){continue;} // Skips the value //
 else {cout << i} }

Same explanation goes in while

string name;
    cout<<"Enter your name :" ;
    getline(cin, name);
    cout<<"Hello "<<name;

std::string a;
	std::cin >> a;
	for( int i=a.size()-3 ; i >0; i= i-3 )
	{   a.insert(i ,",");   }
	std::cout << a;
	
#include <iomanip>
	cout << std::fixed<< m 


```C++
#include <iostream>
#include <string>
int main()
{
std::string a,b;
std::cin >> a >> b;

    std::sort(a.begin(),a.end());
    std::sort(b.begin(),b.end());

    if ( a==b)
    {
        std::cout << "Yes";
    }
    else { std::cout << "No";}

    return 0;
}

#include <bits/stdc++.h>
using namespace std;

int main()
{
    ios_base::sync_with_stdio(false);
    cin.tie(NULL);
    return 0;
}

int main ()
{
int a = 10, b= 11, c= 12;
int d = (a<b); // If the conditional statement is true, 1 will be stored in d
int e = (b>c); // If the conditional statement is false, 0 will be stored in e
}

int main()
{
 int a,b;
 while (cin>>a>>b) { cout << a+b; }
}
```
```C++
int main(){
    freopen("input.txt","r",stdin);
    freopen("output.txt","w",stdout);
    // Your code goes here.
    return 0;
}

int arr[] = {1, 7, 4, 5, 2}; 
    for(auto x : arr)  // We can enter "int" as well in here
    { cout << x << " ";}
// By putting "return 0;" in anywhere, we can terminate the program. After this line, no line of code will be executed    

```
# Programming | Finding maximum value in an array #

This is the code : 

```C++
#include <iostream>
int main()
{
    int a;   
    std::cin >> a;    
    int ar[a];
    for (int i=0; i<a; i++){  std::cin >> ar[i]; }
    int max = 0;
    for (int k=0; k<a; k++) { if( max< ar[k]) { max = ar[k];} }
    std::cout << max;
    return 0; 
}
```

# Sorting-an-array-in-ascending-order #
```C++
#include <bits/stdc++.h>
 using namespace std;
 int main()
{
    int x;
    cin>>x;
    int arr[x];
    for(int i = 0;i<x;i++)cin>>arr[i];
    sort(arr,arr+x);
    for(int i = 0;i<x;i++)cout<<arr[i]<<" ";
    return 0;   
}
```

```C++
#include <iostream>
using namespace std;
int main()
{
    int n,i,j,m;
    cin>>n;
    int a[n];
    for(i=0;i<n;i++)
    {
        cin>>a[i];
    }
    for(i=0;i<n;i++)
    {
        for(j=i+1;j<n;j++)
        {
            if( a[i] > a[j] )
            {
                m=a[j] ; a[j] = a[i]; a[i]=m;
            }
        }
    }

    for(i=0;i<n;i++)
    {
        cout<<a[i] << " " ;
    }
    return 0;
}
```
