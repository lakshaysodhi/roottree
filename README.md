# roottree

#include <bits/stdc++.h>
using namespace std;




int main()
{
    int t;
    cin>>t;
    while(t--){
        int n;
        cin>>n;
        vector<vector<int> > A(n+1);
        int x,y;
        for(int i=1;i<n;i++){
            cin>>x>>y;
            A[x].push_back(y);
        }
        int count1=0;
        unordered_map<int,int> H;

        for(int i=1;i<=n;i++){
                

            for(int j=0;j<A[i].size();j++){
                if(H.count(A[i][j])==0)
                H[A[i][j]]++;
                else {
                    
                        count1++;
                        
                    }
            }
        }

        cout<<count1<<endl;

    }
    return 0;
}
