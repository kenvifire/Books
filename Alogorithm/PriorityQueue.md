# PriorityQueue

## APIs
<code> public class MaxPQ<Key extends Comparable<Key>></code>
* `MaxPQ`					create an empty priority queue
* `MaxPQ(Key[] a)`		create a priority queue with given keys
* `void insert(Key v)`	insert a key into the priority queue
* `Key delMax()`		return and remove the largest key
* `boolean isEmpty()`	is the priority queue empty?
* `key max()`			return the largest key
* `int size()`			number of entries in the priority queue

### unordered array implementation

<pre><code>
public class UnorderedMaxPQ<Key extends Comparable<Key>>
{
	private Key[] pq;
	private int N;

	public UnorderedMaxPQ(int capacity)
	{ pq = (Key[]) new Comparable[capacity]; }

	public boolean isEmpty(){
		return N == 0;
	}

	public void insert(Key x){
		pq[N++] = x;
	}
	public Key delMax(){
		int max = 0;
		for(int i=1;i<N;i++)
			if(less(max,i)) max = i;
		exch(max,N-1)
		return pq[--N];	
	}
}
</code></pre>

## binary heaps

### Complete binary tree
*Binary tree* Empty or node with links to left and right binary trees.
*Complete tree* Perfectly balanced,except for bottom level.

### binary heap representations

*Binary heap* Array representation of a heap-ordered complete binary tree.

Heap-ordered binary tree
* Keys in nodes
* Parenent's key no smaller than children's key

Array represiontation
* Indices start at 1
* Take nodes in level order.
* No explicit links needed

Proposition 
* Largest key is a[1],which is root of binary tree
* Can use array indices to move through tree
	* Parent of node at k is at k/2
	* Children of node at k are 2k and 2k+1

### Promotion in a heap

> Scenari: Child's key becomes *larger* than its parent's key


To eliminate the violation:
* Exchange key in child with key in parent
* Repeat until heap order restored

### Insertion in a heap
> Insert : Add note at end, then swim it up
  Cost : At most 1 + lgN Compares


### Demotion in a heap
> Scenario : Parent's key becomes smaller than one (or both) of its children

To eliminate the violation:
* Exchange key in in parent with key in larger child
* Repeate until heap order restored

### Delete the maximun in a heap
>Delete max : Exchange root with node at end ,then sink it down
 Cost : At most 2lgN compares

 


