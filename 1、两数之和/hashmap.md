```javascript
/**
 * @param {number[]} nums
 * @param {number} target
 * @return {number[]}
 */
var twoSum = function(nums, target) 
{
    let hash = new Map()
    for(let i= 0; i<nums.length;i++)
    {
        hash.set(nums[i],i)
    }
    for(let i = 0;i<nums.length;i++)
    {
        if(hash.get(target-nums[i]) === undefined)
            continue
        else if(hash.get(target-nums[i]) === i)
            continue
        else
            return [i,hash.get(target-nums[i])]
    }
};
```

