# Susie's portfolio
---
---
## PROGRAMMING
### method to create a recursive fence post of size n
```
/**
 * Recursion Practice with Strings by Team SweatEquity
 * Jessica Novillo Argudo
 * collaborators: Saranii Muller, Joel Bianchi, Kirk Martin
 */

public class Fence
{
/**
   String fenceR(int) -- recursive fence generator
   precond:  input is a positive integer
   postcond: returns fence with n posts

   eg
   fenceR(1) -> "|"
   fenceR(2) -> "|--|"
  */
  
public static String fenceR( int n ){

  // BASE CASE: if n is 0, then return ""
  if (n==0){
    return ""; 
  }
  // BASE CASE: if n is 1, then return "|"
  else if (n==1){
    return "|";
  }
  // RECURSIVE CASE: Call fenceR with n-1 and add it to "|--"
  else {
    return "|--" + fenceR(n-1);
  }
    
}
```

---
## DATA STRUCTURES
### method to recursively binary search
```
// binarySearchRecursive() runs a recursive binary search on an ArrayList to find the index of a given value
public int binarySearchRecursive(int value, int lowIndex, int highIndex) {

  if (highIndex - lowIndex != 1) {

    int middleIndex = (lowIndex + highIndex) / 2;

    if (data.get(middleIndex) == value) {
      return middleIndex;
    }

    if (data.get(middleIndex) < value) {
      return binarySearchRecursive(value, middleIndex, highIndex);
    }

    return binarySearchRecursive(value, lowIndex, middleIndex);
  }

  return -1;
}
```
---
## METHODS
### lesson plan for if/else conditionals
[IF/ELSE Conditionals](https://replit.com/@RACHELKAUFMAN/cohort-3-summer-work-rkaufman8#methods/01_lessonplan.pdf)

---
## TO DO
- [x] create my page
- [ ] get CS license
- [ ] ???
- [ ] profit
