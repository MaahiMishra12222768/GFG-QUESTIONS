int solve(vector<vector<int>> &keypad, int i, int j, int n,  vector<vector<vector<int>>> &dp)
    {
    
        
        if(i < 0 || i >= keypad.size() || j < 0 || j >= keypad[0].size() || keypad[i][j] == -1)
            return 0;
            
        if(n == 1)
            return 1;
        
        if(dp[i][j][n] != -1)
            return dp[i][j][n];
        int ans = 0;
        
        int dx[] = {-1,0,0,1};
        int dy[] = {0,1,-1,0};
        ans += solve(keypad,i,j,n-1,dp);
        for(int k = 0; k < 4; k++)
        {
            int new_x = i + dx[k];
            int new_y = j + dy[k];
            ans += solve(keypad, new_x, new_y, n-1, dp);
        }
        return dp[i][j][n]=ans;
    }
    int getCount(int n) 
    {
        vector<vector<int>> keypad = {{1,2,3},
                                      {4,5,6},
                                      {7,8,9},
                                      {-1,0,-1}
                                     };
        vector<vector<vector<int>>> dp(4, vector<vector<int>>(3, vector<int>(16,-1)));                             
        int ans = 0;
        for(int i = 0; i < 4; i++)
        {
            for(int j = 0; j < 3; j++)
            {
                ans += solve(keypad,i,j,n,dp);
            }
        }
        return ans;
        // code here
        
    }

