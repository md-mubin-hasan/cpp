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

[Problem link: ](https://codeforces.com/problemset/problem/26/A)

```C++
//my solution

bool is_prime(int n){
    if(n==1) return false;
    if(n==2) return true;
    if(n%2==0) return false;
    for(int i=3; i*i<=n; i+=2){
        if(n%i==0) return false;
    }
    return true;
}

bool is_almost_prime(int n){
    int cnt=0;
    for(int i=1; i<=n; i++){
        if(n%i==0 && is_prime(i)) cnt++;
    }
    if(cnt==2) return true;
    return false;
}

int main(){
    int n; cin>>n;
    int ans=0;
    for(int i=1; i<=n; i++){
        if(is_almost_prime(i)) ans++;
    }
    cout<<ans;
    return 0;
}

//better solution

const int N = 3030;

bool is_prime[N];
bool check_prime(int n) {
  if (n == 1) return false; // 1 is not a prime by definition
  for (int i = 2; i < n; i++) {
    if (n % i == 0) { // n is divisible by i but i is neither 1, nor n, so n must not be a prime
      return false;
    }
  }
  return true;
}
bool is_almost_prime(int n) { // Level 2
  int prime_divisor_count = 0;
  for (int i = 1; i <= n; i++) {
    if (n % i == 0) { // i is a divisor
      if (is_prime[i]) { // prime divisor (check if it is a prime from the answer array that we precalculated!)
        prime_divisor_count++;
      }
    }
  }
  if (prime_divisor_count == 2) return true; // almost prime when it has two prime divisors
  else return false;
}
int main() {
  int n; cin >> n;
  for (int i = 1; i <= n; i++) {
    is_prime[i] = check_prime(i);
  }

  int ans = 0;

  for (int i = 1; i <= n; i++) {
    if (is_almost_prime(i)) {
      ++ans;
    }
  }
  cout << ans << '\n';
  return 0;
}
```

Day 2
