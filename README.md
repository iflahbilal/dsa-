# findequilbriu index no-

#include <bits/stdc++.h>
int findEquilibriumIndex(vector<int> &arr) {
    
    vector<int>left;
    vector<int>right;
    int sum1=0;
    int sum2=0;
    for(int i=0 ; i<arr.size(); i++)
    {
        sum1=sum1+arr[i];
        left.push_back(sum1);
        
    }
       for(int i=arr.size()-1 ; i>=0; i--)
    {
        sum2=sum2+arr[i];
        right.push_back(sum2);
       
    }
    reverse(right.begin(), right.end());
    for(int i=0;i<arr.size();i++)
    {
        if(left[i]==right[i])
        {
          return i;
        }
       
    }
    return -1;
}
