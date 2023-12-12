#Daa #College #notes 

``` 
QUICKSORT (A, left, right):
	if left < right:
		final_pivot_pos = PARTITION(A, left, right)
		QUICKSORT(A, left, final_pivot_pos - 1)
		QUICKSORT(A, final_pivot_pos + 1, right)
```

PARTITION(A, left, right):
- Will **pick one element** in array **A** from index *left* to *right* as a **pivot** 
- Will **permute** the array **A** from index *left* to *right* in some way such that:
	- elements $<=$
	- 