class Solution {
public:
    vector<int> topKFrequent(vector<int>& nums, int k) {
        
        int n =nums.size();
        vector<int> result;
        unordered_map<int, int> freq;

        for(int i=0; i<n; i++)
        {
            freq[nums[i]]++;
        }

        vector<vector<int>> bucket(n+1);

        for(auto& it : freq)
        {
            int element = it.first;
            int frequency = it.second;

            bucket[frequency].push_back(element);
        }

        for(int i=n; i>=0; i--)
        {
            if(bucket[i].size() == 0)
            continue;

            while(bucket[i].size() > 0 && k > 0)
            {
                result.push_back(bucket[i].back());
                bucket[i].pop_back();
                k--;
            }

            if(k==0)
            break;
        }

        return result;
        
    }
};
