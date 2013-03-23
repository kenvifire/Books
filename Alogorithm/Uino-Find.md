
##Dynamic Connectivity

###Problem

Given a set of N objects
*Union command:connect two objects
*Find/connected query:is there a path connecting the two objects?

## Modeling the objects

Applications involve manipulating objects of all types
* Pixels in a digital photo.
* Computers in a network.
* Friends in a social network.
* Transistors in a computer chip.
* Elements in a mathematical set.
* Variable names in Fortran program.
* Metallic sites in a composite system.

When programming,convenient to name objects 0 to N-1
* Use integers as array index.
* Suppress details not relevant to union-find

We assume "is connected to " is an equivalenc relation:
* Reflexive: p is connected to p.
* Symmetric: if p is connected to q,then q is connected to p.
* Transitive: if p is connected to q and q is connected to r,
  then p is connected to r.

 Implementing the operations
 *Find query:Check if two objects are in the same component.
 *Union command:Replace components containing two objects with their union.


 API
 * UF(int N) initialize union-find data structure with N objects(0 to N-1)
 * void union(int p, int q) add connection between p and q
 * boolean connected(int p ,int q) are p and q in the same component?
 * int find(int p) component identifier for p(0 to N-1)
 * int count() number of components

 ## Quick-find

 Data structure
 * Integer array id[] of size N.
 * Interpretation: p and q are connected if they have the same id.

 ![quick find](pics/quick-find-1.jpg)

