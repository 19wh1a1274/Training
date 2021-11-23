Given a signed 32-bit integer x, return x with its digits reversed. If reversing x causes the value to go outside the signed 32-bit integer range [-231, 231 - 1], then return 0.

Assume the environment does not allow you to store 64-bit integers (signed or unsigned).

 

Example 1:

Input: x = 123
Output: 321

**Solution:**

class Solution 

{

public:

    int reverse(int x) {
    
        int r,s=0;
        
        while(x !=0)
        
        {
        
            r = x %10;
            
            if(s > INT_MAX/10)
            
            {
                return 0;
                
            }
            
            if(s < INT_MIN/10)
            
            {
                return 0;
                
            }
            s = s*10+r;
            
            x = x/10;
        }
        
        return s;
        
    }
};
