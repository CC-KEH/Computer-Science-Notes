```rust
impl Solution {
    pub fn two_sum(nums: Vec<i32>, target: i32) -> Vec<i32> {

        use std::collections::HashMap; // Import

        let mut num_map : HashMap<i32, i32> = HashMap::new();

        for (i, num) in nums.iter().enumerate(){ // iter gives reference

// here i, num are a references (&i32, &i32), so num has to be deref for operation.
            match num_map.get(&(target - *num)){ // * => deref, & => ref

// You only access, ref of a val in hashmap, 
                Some(&i2) => return vec![i as i32, i2 as i32],

// Insert into hashmap a new value, so deref the val => i32
                None => num_map.insert(*num, i as i32),
            };
        }
        vec![] // return a empty vec
    }
}
```
