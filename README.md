# nge-stack



#include<bits/stdc++.h>
#define int long long int
using namespace std;
signed main()
{
int t;
cin>>t;
while(t--){int n,co=0,ro=0,go=0;
cin>>n;
int a[n];
for(int i=0;i<n;i++)cin>>a[i];
int nge[n];
stack<int>st;
for(int i=n-1;i>=0;i--){
    while(!st.empty() && st.top()<=a[i%n]){
st.pop();
    }
    if(i<n-1){
        if(st.empty()==false)nge[i]=st.top();
        else nge[i]=-1;
    }
     else nge[i]=-1;

    st.push(a[i%n]);
}

for(int i=0;i<n;i++){cout<<nge[i]<<" ";}
}
 return 0;
}
