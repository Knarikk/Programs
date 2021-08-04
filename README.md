# Programs
//Աջ տեղաշարժ k քայլով
#include <iostream>
#include<vector>
using namespace std;

void rotate(unsigned int k, vector<int>& v)
{
    if (v.size() < k) 
            return;
    std::vector<int> temp;
    for (unsigned i = 0; i < k; ++i)
    {
        temp.push_back(v[v.size()-1-i]);
    }
    for (unsigned i = v.size()-1; i >= k; --i) 
    {
        v[i] = v[i-k];
    }
    for (unsigned i = 0; i < k; ++i) 
    {
        v[i] = temp[i];
    }
    
   for (unsigned i = 0; i < v.size(); ++i) 
    {
        cout<<v[i]<<" ";
    }


}
int main()
{      
    vector<int>v  = {100,100,56,-1,0,-1};
            rotate(3, v);
    return 0;
}
