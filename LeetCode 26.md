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
#### 2改：
```
var removeDuplicates = function (nums) {
var len = nums.length;
if(len<2) return len;
var ipos = len-2;
var numval = nums[len-1];
while(ipos >= 0){

if(nums[ipos]===numval){
var dupStat = ipos;
while(ipos>=0 && nums[ipos]===numval)ipos--;
nums.splice(ipos+1,dupStat-ipos);


}else{
numval = nums[ipos];
ipos--;
}

}
return nums.length;
};
```

### 返回数组的长度，跨越长度的不用管。。

```
var removeDuplicates = function (nums){
var len = nums.length;
if(len < 2){
return len;
}
var j = 0;
for(var i = 1;i<len;i++){
if(nums[j] !== nums[i]){
j++;
nums[j]=nums[i];
}
}
return ++j;
};
```


##### 心得：看懂题。。
