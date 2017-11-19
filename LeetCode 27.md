# LeetCode 27
###### 题目：Remove Element
###### 难度：easy

```
var removeElement = function(nums, val) {
    var index = nums.indexOf(val);
    if(index === -1) {
        return nums.length;
    }else {
        while(index !== -1){
            nums.splice(index,1);
            index = nums.indexOf(val);
        }
        return nums.length;
    }
};
```

