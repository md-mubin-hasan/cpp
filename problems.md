Day 1

[Problem link: ](https://atcoder.jp/contests/abc226/tasks/abc226_a) [Rounding without using builtin function](https://atcoder.jp/contests/abc226/editorial/2903)

[Problem link: ](https://codeforces.com/problemset/problem/633/A) 

```C++
//my solution

int a,b,c;
cin>>a>>b>>c;
for (int i = 0; i <= 10000; i++)
    {
        for (int j = 0; j <= 10000; j++)
        {
            x = a*i + b*j;
            if(x == c){
                cout<<"Yes";
                return 0;
            }
        }
    }
cout<<"No";

//better solution

int evony_damage, ivory_damage, damage_goal;
cin >> evony_damage >> ivory_damage >> damage_goal;

// evony and ivory can do any non-negative number of shots
// so lets try all possible shots
for (int evony_shots = 0; ; evony_shots++) {
    if (evony_shots * evony_damage > damage_goal) {
      break; // it doesn't make sense to loop further as the damage is already more than our goal
      }
    for (int ivory_shots = 0; ; ivory_shots++) {
      int total_damage = evony_shots * evony_damage + ivory_shots * ivory_damage;
      if (total_damage == damage_goal) { // yayy
        cout << "Yes\n";
        return 0; // return immediately
        }
      if (total_damage > damage_goal) { // no need to take more shots, its already bigger
        break;
        }
    }
}

// we are here means we haven't met the damage goal
cout << "No\n";
```

[Problem link: ](https://codeforces.com/problemset/problem/102/B)

```C++
long long int sum_of_digits(long long int n){
    long long int sum = 0;
    while(n>0){
        sum += n%10;
        n /= 10;
    }
    return sum;
}

int main(){
    char s[100005]; cin>>s;
    long long int n = strlen(s);
    long long digit_sum = 0, ans = 0;
    if(n==1){
        cout<<0;
        return 0;
    }
    for(int i=0; i<n; i++){
        digit_sum += s[i]-'0';
    }

    while(digit_sum > 9){
        digit_sum = sum_of_digits(digit_sum);
        ans++;
    }
    cout<<ans+1;
    return 0;
}
```
