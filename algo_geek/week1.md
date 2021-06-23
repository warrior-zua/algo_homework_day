/*加一*/

class Solution  {
public:
    vector<int> plusOne(vector<int>& digits) {
        for(int i=digits.size()-1; i>=0; i--)
        {
            digits[i]++;
            if(digits[i] == 10)  digits[i] = 0;
            else  return digits;
        }
        digits.insert(digits.begin(), 1);
        return digits;
    }
};



/*和为K的子数组*/

class Solution {
public:
    int subarraySum(vector<int>& nums, int k) {
        int count = 0;
        for (int start = 0; start < nums.size(); ++start) {
            int sum = 0;
            for (int end = start; end >= 0; --end) {
                sum += nums[end];
                if (sum == k) {
                    count++;
                }
            }
        }
        return count;
    }
};

