# LeetCode 26
###### 题目：Remove Duplicates from Sorted Array
###### 难度：easy

```
var removeDuplicates = function(nums) {
            var len = nums.length;
            var numpos= nums.length - 1;
            var ipos = nums.length -2;
            var flag = 0;
            if(len<2) return nums.length;

            for( ;ipos>=0;ipos--){
                if(nums[ipos] === nums[numpos]){
                    flag = 1;
                    if(ipos===0){
                        nums.splice(ipos+1,numpos-ipos);
                        break;
                    }
                }else{
                    if(flag===1){
                        nums.splice(ipos+2,numpos-ipos-1);
                    }
                    numpos = ipos;
                    flag = 0;
                }


            }
            return nums.length;


        };
```
