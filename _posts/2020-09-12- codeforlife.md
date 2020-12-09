---
layout: post
title: Computer Science 
subtitle: (Problem Solving 3)
//cover-img: /assets/img/115d1ec4-32fd-4516-812d-8f77508ac9b4.jpeg
//thumbnail-img: /assets/img/115d1ec4-32fd-4516-812d-8f77508ac9b4.jpeg
//share-img: /assets/img/115d1ec4-32fd-4516-812d-8f77508ac9b4.jpeg
tags: [tutorial]
---

### Problem 3.01
```c++

int fibo(int x){
int f0 = 0;
    int f1 = 1;
    int fn = 1;
    int i;

    if (x<=0||x>30) {
    } else if (x == 0 || x == 1) {
        return x;
    } else {
        for (i = 2; i < x; i++) {
            f0 = f1;
            f1 = fn;
            fn = f0 + f1;
        }
    }
    return fn;
}

```
### Problem 3.04
```

int main(){
    int a,b,n,s1=0;
    cin>>a>>b>>n;
    while(n!=0){
    s1+=a*b;
    a++;
    b++;
    n--;}
    cout<<s1;
}
```
### Problem 3.05
```

double s1(double n)
{
    double s=0;
    for(int i=1; i<=n; i++)
    {
        s=s+(double)pow(i,i);
    }
    return s;
}
double s2(double n)
{
    double t=1;
    double s=0;
    for(int i=1; i<=n; i++)
    {
        t=t*i;
        s=s+t;
    }
    return s;
}
double s3(double n)
{
    double s=0;
    double t=0;
    for(int i=1; i<=n; i++)
    {
        t=t+i;
        s=s+1/t;
    }
    return s;
}
```
### Problem 3.06
```

long long Sum1(int x, int n)
{
    long long s=1,t=1;
    for(int i=1; i<=n; i++)
    {
        t=t*x;
        s=s+t;
    }
    return s;
}
float Sum2(int x, int n)
{
    //1+x^2+x^4 ++x^2n
    float s=1,t=1;
    for(int i=1; i<=n; i++)
    {
        t=t*x*x;
        s=s+t;
    }
    return s;
}
double Sum3(int x, int n){
    double s=1,t=1,m=1;
    int i=1;
    while(i<=n)
    {
        t=t*x;
        m=m*i;
        s=s+t/m;
        i++;
    }
    return s;
}

```
### Problem 3.07
```

float sopi(int n){
    float t,m;
    float s=0;
    for(int i=0; i<=n; i++){
        t=pow(-1,i);
        m=(2*i)+1;
        s=s+(4*(t/m));
    }
    return s;
}

```
### Problem 3.08
```

    int n,t,s=0;
    cin>>n;
    while(n!=0){
        t=n%10;
        s+=t;
        n/=10;
    }
    cout<<s;
    return 0;
}
```
### Problem 3.10
```
#include <bits/stdc++.h>
#define MAX 1000
using namespace std;
int main()
{
  int a[MAX];
  int idx = 0;
  int n,d=0;
  cin>>n;
  for (int i = 1; i < n; ++i)
  {
    int val = i/2;
    bool no_div = true;
    for (int j = 2; j <= val; ++j)
    {
      if (i%j == 0)
      {
        no_div = false;
        break;
      }
    }

    if (no_div == true)
    {
      a[idx] = i;
      idx++;
    }
  }
  for (int t = 0; t < idx-1; t++)
  {
    int n1 = a[t];
    int n2 = a[t+1];
    if ((n2-n1) == 2)
    {
      cout << n1 << ", " << n2;
      cout << "\n";
      d++;
    }
  }
  cout<<"Tong: "<<d<<" cap so sinh doi < "<<n;
  return 0;
}
```
### Problem 4.01
```

long sum_even_divisor(int n){
    long s=0;
    if(n!=0){
    for(int i=2; i<=n; i=i+2){
        if(n%i==0){
            s+=i;
    }}
    if(s==0) s=-1;
}
else s=-1;
  return s;
}
```
### Problem 4.02
```
#include<math.h>
long sum_all_square(int n){
    int s=0;
    for(int i=1; i<=n; i++){
            int d=sqrt(i);
        if(n%i==0 && d*d==i){
            s=s+i;
        }
    }
    return s;
}
```
### Problem 4.03
```


long TongUocChung(int a, int b){
    int s=0;
    int m=min(a,b);
    for(int i=1; i<=m; i++){
        if(a%i==0 && b%i==0){
            s=s+i;
        }
    }
    return s;
}

```
### Problem 4.04
```
bool ktr(int n)
{
    if (n <= 1)  return false;
    if (n <= 3)  return true;
    if (n%2 == 0 || n%3 == 0) return false;

    for (int i=5; i*i<=n; i=i+6)
        if (n%i == 0 || n%(i+2) == 0)
           return false;

    return true;
}
long sum_common_prime(int a, int b){
    int s=0;
    int m=min(a,b);
    if(a!=0 && b!=0){
            for(int i=1; i<=m; i++){
                if(ktr(i)==1 && a%i==0 && b%i==0) s=s+i;
            }
    }
    if(s==0) s=-1;
    return s;
}
```
### Problem 4.07
```

double calculate(int n){
    double s=sqrt(1.0);
    for(int i=2; i<=n; i++){
            float t=i+s;
        s=sqrt(t);
    }
    return s;
}
```
### Problem 4.08
```
×

int reverse(int n){
    int tmp;
    int res=0;
    while(n>0){
        tmp=n%10;
        res=res*10+tmp;
        n=n/10;
    }
    return res;
}
```
### Problem 4.09
```python
    404
ERROR
```
### Problem 4.10
```

int main(){
    int n;
    cin>>n;
    long s=1;
    for(int i=1; i<=n; i++){
        if(n%2==0){
            s=s+(s*i);
        }
        else s=s*i;
        i++;
    }
    cout<<s;
    return 0;
}
```
### OP
```c#
while(i <= sqrt(m))
    {
        if(m%i==0) {
            //cout<<i<<" ";
            if(ktr(i)==1 && n%i==0) s1=s1+i;
            if (i != (m / i)) {
                    int a=m/i;
                //cout<<a<<" ";
                if(ktr(a)==1 && n%a==0) s2=s2+a; //cout<<s2<<" ";
            }
        }

        i++;
    }
```
### Credit: Trương Văn Sỹ
### Contact:[FB](https://fb.com.vn/hvcsndhn)
