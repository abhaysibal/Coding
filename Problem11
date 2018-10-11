// Self Note @Abhay: Problem is similar to how error reduction happens in neural networks and linear/logistic classifiers.
// We start with some error E, and have to minimize it to work towards reaching the final error free state. In this case the area is what we 
// have to maximize. Now area is a function of two independent parameters : distance in X Axis and Y Axis. We start with maximum value of the 
// independent parameter X and then carefully adjust Y to attain maxima. If we are reducing in X, then obviously we should be gaining in Y, 
// hence the intuition of advancing the index which is having a lower value than the other index.

class Solution {
public:
    int maxArea(vector<int>& height) {
        long long int l_index = 0;
        long long int r_index = height.size() - 1;
        
        long long int max_area = 0;
        while(l_index < r_index)
        {
            max_area = max(max_area, (long long int)(std::min(height[l_index] , height[r_index]))*(r_index - l_index));
            if(height[l_index] < height[r_index])
                l_index ++;
            else
                r_index --;
        }
        return max_area;
    }
};
