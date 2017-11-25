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
展开。感觉自己棒棒哒！
```

var zhankai = function (arr) {
    var arr2 = [] ;
    for(var i =0;i<arr.length;i++){
       if(typeof(arr[i])!== "number"){

           var flag = zhankai(arr[i]);
           arr2 = arr2.concat(flag);

       }
       else {
           arr2.push(arr[i]);

       }
    }
    return arr2;

};
var beauty = [2,[3,[6,7],4,5],5,[8,9,2,[3,4]],9];
console.log(zhankai(beauty));

```

