## Patterns in Subsets Problems:
### [[DSA/Recursion/Subsequence|Same as Subsequence]]

## Generating Subsets using Recursion
```java
static ArrayList<String> ans = new ArrayList<>(); //Better approach

static ArrayList<String> func(String processed,String Unprocessed){
	if(Unprocessed.length==0){
		ArrayList<String> ans = new ArrayList<>(); //not good
		ans.add(processed);
		return ans;
	}
	char ch = Unprocessed.charAt(0);
	ArrayList<String> left = func(processed,Unprocessed.substring(1));
	ArrayList<String> right = func(processed+ch,Unprocessed.substring(1));
	left.addAll(right);
}
```

