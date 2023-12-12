#Daa #College #notes 

# Recursion - Tree

``` 
Idea: Draw the recursion-tree then 
“creatively” bound the total runtime
```

![[Pasted image 20231011132309.png]]

- How to find max level
	- dependent on the function
	- Biasanya bisa dengan menganalisa kapan rekursi akan sampai ke 1, 
	  contoh:
	  jika 
- Cost calculation
	- sum dari semua cost per level
- upper-bound
	- sum cost per level * max height
# Substitution

```
Guess the answer then inductively verify it
```

$$
example : 𝑇 (𝑛) = 2𝑇 (𝑛/2) + 𝑛
$$
$$
guess : O(n logn)
$$
> Verify by induction
![[Pasted image 20231011133356.png]]
# Master Theorem
![[Master Theorem.canvas]]
# Telescoping (Optional)