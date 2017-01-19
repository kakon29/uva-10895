# uva-10895
#include<bits/stdc++.h>

using namespace std;

vector< pair<int,int> >v2[10001];

int main()
{
    int m,n;

    while(cin >> m >> n)
    {
       // cin.ignore();
        for(int i=0;i<=10000;i++)
            v2[i].clear();
         int c = 0;
         int row=0;
        for(int i=1;i<=m;i++)
        {
            row++;
           int k;
           cin >> k;
           int a[k+1];
           for(int i=1;i<=k;i++)
            cin >> a[i];
           for(int i=1;i<=k;i++)
           {
               int x;
               cin >> x;
               v2[a[i]].push_back(make_pair(row,x));
           }



        }
        cout << n << " " << m << endl;
        for(int i=1;i<=n;i++)
        {
            if(v2[i].size()>0)
            {
                cout << v2[i].size() << " ";
                for(int j=0;j<v2[i].size();j++)
                {
                    if(j==(v2[i].size()-1))
                        cout << v2[i][j].first << endl;
                    else
                        cout << v2[i][j].first << " ";
                }

                for(int j=0;j<v2[i].size();j++)
                {
                    if(j==(v2[i].size()-1))
                        cout << v2[i][j].second << endl;
                    else
                        cout << v2[i][j].second << " ";
                }
            }
            else
            {
                cout << "0\n";
                cout << endl;
            }
        }
    }
    return 0;
}

