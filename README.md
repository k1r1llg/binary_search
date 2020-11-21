#include <iostream>
#include <algorithm>
#include <string>
using namespace std;
 
int main()
{
    ios::sync_with_stdio(0);
cin.tie(0);
cout.tie(0);
    int n, m;
    cin>>n>>m;
 
 
    int a[n];
    for(int i=0; i<n; i++) {
        cin>>a[i];
    }
 
    sort(a, a+n, less<int>{});
    for(int i=0; i<m; i++) {
            int x;
    cin>>x;
        int l=0, r=n-1;
        int f=0;
            while(r-l>=0){
                int c=(l+r)/2;
 
 
        if(x==a[c]) {
 
            f=1;
            break;
        }
        else if(a[c]<x) {
            l=c+1;
        }
        else if(a[c]>x) {
            r=c-1;
        }
 
 
    }
     if(f==0) {
            cout<<"No"<<"\n";
        }
         else {
            cout<<"Yes"<<"\n";
        }
    }
}
