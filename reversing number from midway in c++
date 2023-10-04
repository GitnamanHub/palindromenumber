class Solution {
public:
    bool isPalindrome(int x) {
        if(x<0)
        return false;
        int digits{};
        int temp{x};
        while(temp>0){
        temp/=10;
        digits++;
        }
        double mid=digits/2;
        int firsthalf=x / pow(10.0,mid);
        int secondhalf = x % static_cast<int>(pow(10.0,mid));
        temp=secondhalf;
        int secondhalfdigits{};
        while(temp>0){
        temp/=10;
        secondhalfdigits++;
        }
        int zero{};
        if(digits%2)
        {
            zero = digits-mid-secondhalfdigits-1;
        }
        else
        {
            zero = digits-mid-secondhalfdigits;
        }
        int reverse{};
        temp=secondhalf;
        while(temp>0)
        {
            int reminder = temp % 10;
            reverse = reverse *10 + reminder;
            temp/=10;
        }

        if(digits%2)
        {
            firsthalf=firsthalf/10;
        }
        for(int i=zero;i>0;i--)
        {
            reverse*=10;
        }

        return (firsthalf==reverse);
    }
};
