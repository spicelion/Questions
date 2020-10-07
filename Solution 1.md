Solution 2

#include<bits/stdc++.h>
using namespace std;
#define ll long long
#define MOD 1000000007

int factorial(int n){
	if(n==1 || n==0)
	return 1;
	int f=1;
	for(int i=2;i<=n;i++)
	f=f*i;
	return f;
}

int main(){
	fast;
	int t;
	cin>>t;
	while(t--){
		int n,i;
		cin>>n;
		int arr[n];
		for(i=0;i<n;i++)
		cin>>arr[i];
		ll fact=factorial(n);
		ll digitsum=0;
		for(i=0;i<n;i++)
		digitsum+=arr[i];
		digitsum*=(fact/n);
		ll k=1;
		ll res=0;
		for(i=0;i<n;i++){
			res+=(k*digitsum);
			k*=10;
		}
		cout<<res<<"\n";
	}
	return 0;
}