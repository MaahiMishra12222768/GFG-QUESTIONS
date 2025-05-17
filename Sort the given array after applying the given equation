class Solution {
  public:
    vector<int> sortArray(vector<int> &arr, int A, int B, int C) {
        // code here
        vector<int> v;
        for (int x : arr) {
            int calc = (A * x * x) + (B * x) + C;
            v.push_back(calc);
        }
        sort(v.begin(), v.end());
        return v;
    }
};
