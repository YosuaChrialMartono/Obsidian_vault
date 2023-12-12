#Daa #College #notes 

# Binary Heap

## Binary (max) Heap
- Is a complete (**not full**) rooted binary tree
- All vertices satisfy **max-heap property**
- **Max-Heap property**
	- The vertex (parent) value ≥ Its children’s values
![[Pasted image 20231011134041.png]]

## Binary (min) Heap
- Is a complete (**not full**) rooted binary tree
- All vertices satisfy **min-heap property**
- **Min-Heap property**
	- The vertex (parent) value ≤ Its children’s values
 ![[Pasted image 20231011134346.png]]

## Binary heap implementation
![[Pasted image 20231011134420.png]]
![[Pasted image 20231011134425.png]]

**Parent** of vertex 𝒊 is at index ⌊𝒊 / 𝟐⌋ 
**Left Child** of vertex 𝒊 is at index 𝟐 × 𝒊 
**Right Child** of vertex 𝒊 is at index 𝟐 × 𝒊 + $1$

## Subtree of Binary (max) Heap
- The root of binary max heap is always the maximum element
- The height of a tree is the number of edges from the root to the deepest leaf
- The subtree of a max tree is a max tree

# Operations in Heap
## Bubble Up & Down
### Bubble UP (index)
• The element A[idx] may not satisfy the heap-property w.r.t. its parent 
• Swap with parent and continue BUBBLE_UP from there 
• Time Complexity? Reaching up till the root, 𝑂(𝑙𝑜𝑔 𝑛)

### Bubble Down(index) a.k.a HEAPIFY(index)
- The element A[idx] may not satisfy the heap-property w.r.t. its children
- Swap with the largest child and continue BUBBLE_DOWN from there 
- Time Complexity? 𝑇(𝑛) ≤ 𝑇 (2𝑛/3) + 𝛩(1), therefore: 𝑇(𝑛) = 𝑂(𝑙𝑜𝑔 𝑛)

## More operations
### 1. INSERT(val) : 
> Inserting a new value to the binary heap 
1. Attach the value at the new index: N + 1
2. **BUBBLE_UP**(N + 1)
### 2. FIND_MAX() : 
> Find what is the maximum value in the binary heap  
1. Return A[1]
	time complexity = O(1) 
### 3. EXTRACT_MAX() : 
> Remove the maximum value from the binary heap  
1. Replace A[1] with A[N]
2. **BUBBLE_DOWN**(1)
### 4. BUILD_HEAP(arr) :
> Given any array, create a binary heap from it 
1. Create a new array as a **binary heap**
2. **INSERT** all elements from the input array to the binary heap
Time Complexity? 𝑶(𝑵 𝐥𝐨𝐠 𝑵)
### 5. HEAP_SORT(arr) : 
> Given any array, sort the array (using binary heap)
1. **BUILD_HEAP**(arr)
2. For **N** many times: **FIND_MAX**() + **EXTRACT_MAX**() into a new array
3. The new array will be sorted in descending order, reverse it for ascending order
Time Complexity : 𝑶(𝑵 𝒍𝒐𝒈 𝑵)