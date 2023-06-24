# cpp-commands
These are the C++ concepts which I might need in future 

# Some beginnaer Tricks #

### Operators ###
```C++
!= 3    x = x|3  >>= 3  x= x>>3    <<= 3  x= x<<3
```
```
#include<bits/stdc++.h>
using namespace std;
#define fasty ios_base::sync_with_stdio(false); cin.tie(NULL); cout.tie(NULL);
typedef long long ll;

int main ()
{
    int a = 5;
    int b =  ++a;   // b= 6    a=6
    int c =  a++;   // c= 6    a = 7

cout << a++;     // 7    a=8
cout << ++a;  // 9    a=10

if (negative and positive numbers are regarded as true... only 0 is regarded as false){}
else{}

vector<bool> abc (n); // sob elements jodi true deya hoy and ekta spot e jodi faka thake

for (int i = 0; i < n; ++i) {
        if (!abc[i]) {
            cout << "No\n";
            return 0;  // ekhane eita deya mane code run kora ekhane stop korbe, ei condition ashle
        }

vector<int> A(N);   // integer keo sort kora jay, string keo sort kora jay
sort(A.begin(), A.end());

int bc = c%2 == 1 && b<0;  
}
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

# Converting-all-letters-to-lowercase-or-uppercase-letters #

```C++
#include <iostream>
using namespace std;
int main()
{ 
string a,b;
cin>>a>>b;
transform(a.begin(), a.end(), a.begin(), ::tolower);
transform(b.begin(), b.end(), b.begin(), ::toupper);
}
```

# Count-the-number-of-characters-in-a-string-and-printing-the-maximum-number-of-occurence #

```C++
#include <iostream>
#include <string>
using namespace std;


// Function that return count of the given
// character in the string

int count(string s, char c)
{
// Count variable
int res = 0;
for (int i=0;i<s.length();i++)

// checking character in string
if (s[i] == c)
    res++;

return res;
}

// Driver code
int main()
{
long int a;
cin >> a;
string str;
cin >> str;
char c = 'c';
char o = 'o';
char d = 'd';
char e = 'e';
long int p,q,r,s;
p = count(str, c);
q = count(str, o);
r= count(str, d);
s= count(str, e);
cout <<( (p<=q ? p : q) <= (r<=s ? r : s) ? (p<=q? p : q) : (r<=s ? r : s)  ) << endl;
return 0;
}
```

# Carryout-task-in-alternating-number-in-for-loop #


```C++
int main()
{
bool alternate = true;

for (int x = 0; x < 8; x++)
{
for (int y = 0; y < 4; y++)
{
if (alternate)
{
    std::cout << "X ";
    std::cout << "O ";
}
else
{
    std::cout << "O ";
    std::cout << "X ";
}
}
alternate = !alternate;
std::cout << "\n";
}
```

# Switch-statement #
```C++
#include <iostream>
using namespace std;
string dayoftheweek(int daynumber)
{
string dayname;
switch(daynumber)
{
case 0 : dayname= "Sunday";
break;

case 1 : dayname= "Monday";
break;

case 2 : dayname= "Tuesday";
break;

case 3 : dayname= "Wednesday";
break;

case 4 : dayname= "Thursday";
break;

case 5 : dayname= "Friday";
break;

case 6 : dayname= "Saturday";
break;

default:
    dayname= "Invalid Day Number";
}

return dayname;
}

int main()
{
cout<<"Enter day number : ";
int m;
cin>>m;
cout << dayoftheweek(m);
return 0;
}
```

# nCr-Formula_Efficient-way #
```C++
#include <bits/stdc++.h>
using namespace std;

// Function to find the nCr
void printNcR(int n, int r)
{
// p holds the value of n*(n-1)*(n-2)...,
// k holds the value of r*(r-1)...
long long p = 1, k = 1;

// C(n, r) == C(n, n-r),
// choosing the smaller value
if (n - r < r)
r = n - r;

if (r != 0) {
while (r) {
    p *= n;
    k *= r;

    // gcd of p, k
    long long m = __gcd(p, k);

    // dividing by gcd, to simplify
    // product division by their gcd
    // saves from the overflow
    p /= m;
    k /= m;

    n--;
    r--;
}

// k should be simplified to 1
// as C(n, r) is a natural number
// (denominator should be 1 ) .
}

else
p = 1;

// if our approach is correct p = ans and k =1
cout << p << endl;
}

// Driver code
int main()
{
int a;
cin>>a;
int n = a-1, r = 11;

printNcR(n, r);

return 0;
}
```

# Prime-Factorization-Number

```C++
#include<bits/stdc++.h>

using namespace std;

int main()
{
int num,n,i;
cin>>num;
n=num;
vector <int> fact;
for (i=2;i<=n;)
{
if (n%i==0)
{
    fact.push_back (i);
    n=n/i;
    i=2;
}
else
    i++;
}
for (int j=0;j<fact.size();j++)
{
cout<<fact[j]<<" ";
}
cout <<" = " <<num;
}
```

```
(a+b)%m = (a%m + b%m)%m
(a-b)%m = (a%m - b%m)%m
(a*b)%m = (a%m * b%m)%m
(a/b)%m = (a%m * b^-1%m)%m
(a^b)%m = ((a%m)^b)%m
But not (a/b)%m = (a%m / b%m)%m
```

```
vector<string> msg {"Hello", "C++", "World", "from", "VS Code", "and the C++ extension!"};

for (const string & word : msg)
{
	cout << word << " ";
}
cout << endl;
```

## Pre-computation techniques - hashing
```
#include <bits/stdc++.h>
using namespace std;
//Finding factorial modulo 1e9+7
const int N = 1e5+10;
const int M = 1e9+7;
long long int ar[N];
int main()
{
    int t;
    cin>>t;
    ar[0] = ar[1] = 1;
    for(int i = 2; i<N; ++i ){
        ar[i] = (ar[i-1]*i)%M;
    }
    while(t--){
        int n;
        cin>>n;
        // long long int fact = 1;
        // for(int i = 2; i<=n; ++i){
        //     fact = (fact*i)%M;
        // }
        cout<<ar[n]<<"\n";
    }

    return 0;
}
```

## Pre-computation techniques - prefix sum 1D array
```
#include <bits/stdc++.h>
using namespace std;

const int N = 1e5+10;
long long int ar[N];

int main()
{
    int n;
    cin>>n;
    int arr[n+1];
    ar[0]=0;
    for(int i=1; i<=n; ++i){
        cin>>arr[i];
        ar[i] = ar[i-1] + arr[i];
    }
    int q;
    cin>>q;
    while(q--){
        int l, r;
        cin>>l>>r;
        cout<<ar[r]-ar[l-1]<<"\n";
    }

    return 0;
}
```

## Pre-computation techniques - prefix sum 2D array
```
#include <bits/stdc++.h>
using namespace std;

const int N = 1e3+1;
long long int ar[N][N];

int main()
{
    int n;
    cin>>n;
    int arr[n+1][n+1];
    for(int i=1; i<=n; ++i){
        for(int j=1; j<=n; ++j){
            cin>>arr[i][j];
            ar[i][j] = ar[i-1][j] + ar[i][j-1] - ar[i-1][j-1] + arr[i][j];
        }
    }
    int q;
    cin>>q;
    while(q--){
        int a,b,c,d;
        cin>>a>>b>>c>>d;
        cout<<ar[c][d]-ar[a-1][d]-ar[c][b-1]+ar[a-1][b-1]<<"\n";
    }

    return 0;
}
```

```
#include<bits/stdc++.h>
using namespace std;
int ar[1000002];
main()
{
int n,sum;
cin>>n>>sum;
for(int i=0;i<=1000001;i++)
ar[i]=0;
for(int i=1;i<=n;i++)
{
    int a;
    cin>>a;
    ar[a]++;
}
int left=0; int right=1000001;
bool ans=false;
while(left<right)
{
    if(ar[left]==0||ar[right]==0)
    {
        while(ar[left]==0)
        left++;
        while(ar[right]==0)
        right--;
    }
    if(left+right==sum&&left!=right)
    {
        ans=true; break;
    }
    else if(left+right>sum)
    right--;
    else if(left+right<sum)
    left++;
}
if(left+right==sum&&left==right&&ar[left]>1)
    ans=true;
if(ans)
cout<<"YES";
else
cout<<"NO";
}
```

```
#include <bits/stdc++.h>
using namespace std;

int main()
{
    int t;
    cin>>t;
    int ar[t+1];
    int gcd[t+1];
    gcd[0]=0;
    for(int i=1; i<=t; ++i){
        cin>>ar[i];
        gcd[i] = __gcd(gcd[i-1], ar[i]);
    }
    for(int i=1; i<=t; ++i){
        cout<<gcd[i]<<" ";
    }

    return 0;
}
```

```
#include <bits/stdc++.h>

using namespace std;
const long int M = 1e7+10;
long long int ps[M]={0};
long long int ar[M]={0};
int main()
{
    long int n,q;
    cin>>n>>q;
    while(q--){
        long long int a,b,k;
        cin>>a>>b>>k;
        ar[a] += k;
        ar[b+1] -= k;
    }
    
    for(long int i=1; i<=n; ++i){
        ps[i] = ps[i-1]+ar[i];
    }
    long long int mx = -1;
    for(long int i=1; i<=n; ++i){
        if(mx < ps[i]){mx=ps[i];}
    }
    cout<<mx;
    return 0;
}
```

## Prefix Sum + Hashing Hard Question
```
#include <bits/stdc++.h>

using namespace std;
const int n = 1e5+10;
int hsh[26][n];

int main()
{
    int t;
    cin>>t;
    while(t--){
        int N, Q;
        cin>>N>>Q;
        string s;
        cin>>s;
        for(int i=0; i<26; ++i){
            for(int j=0; j<=N; ++j){
                hsh[i][j] = 0;
            }
        }

        for(int j=0; j<N; ++j){
            hsh[s[j]-'a'][j+1]++;
        }

        for(int i=0; i<26; ++i){
            for(int j=1; j<=N; ++j){
                hsh[i][j] += hsh[i][j-1];
            }
        }
        while(Q--){
            int l,r;
            cin>>l>>r;
            int oddc = 0;
            for(int i=0; i<26; ++i){
                if( (hsh[i][r]-hsh[i][l-1])%2 != 0 ){oddc++;}
            }
            if(oddc > 1){cout<<"No\n";}
            else{cout<<"Yes\n";}
        }
    }

    return 0;
}
```
