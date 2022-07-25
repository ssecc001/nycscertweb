# Susie's portfolio
---
---
## PROGRAMMING
### method to create find index of
```

import java.io.*;
import java.util.*;

  public int indexOf(String value){
    Node walker = head;
    int counter = 0;
    while (walker != null){
      if (walker.getData() == value){
         return counter;
      }
      walker = walker.getNext();
      counter ++;
      }
    return -1;
    }
```

## METHODS
### Here is how to create a Bar Graph
```
import java.io.*;
import java.util.*;

public class BarGraphify {

  public static void main(String[] args){
    ArrayList<Integer> numList= new ArrayList<Integer>();
    //setup the array
    Random random = new Random();
    for (int i  = 0; i < 4; i++){      
      numList.add(random.nextInt(10));
    }
     
    System.out.println(numList);//prints the list
    //[0,1,2,3]
    for(int i = 0; i < numList.size(); i++){
      int barNum = numList.get(i);
      System.out.print(i + ": ");
      for(int j = 0; j<barNum; j++){
        System.out.print("=");
      }
      System.out.println("");
     // System.out.println(numList.get(i)); prints the value at i
        //pretend we are 3, value is 3
        //3 is 3 spots from 0p

      
   }
          
        
      }
} 
```
## DS
### Here is how to Code for ArrayList
```
import java.io.*;
import java.util.*;

/** Methods to write
Basic level:
------------
public static ArrayList<Integer> buildRandomList(int size, int maxval)
public static int sumOfList(ArrayList<Integer> dataList)
Intermediate level:
-------------------
public static void swapElements(ArrayList<Integer> dataList, int indexA,int indexB)
public static void removeValue(ArrayList<Integer> dataList, int valueToRemove)
Advanced level:
-------------------
public static ArrayList<Integer> sumLists(ArrayList<Integer>ListA,ArrayList<Integer>ListB)
public static ArrayList<Integer> zipLists(ArrayList<Integer>ListA,ArrayList<Integer>ListB)
*/


public class AlPractice{

  /**
  Parameters:
  - size - an integer representing how many items to add to the list
  - maxval - the largest value to store in the list
  Preconditions:
  - size >= 0
  - maxVal > 0
  Returns:
  - A new ArrayList of Integers with each value being a random
    number between 0 and maxval (not including maxval).
  */

  // buildRandomList(5,10)
  public static ArrayList<Integer> buildRandomList(int size, int maxval){
    ArrayList<Integer> newList = new ArrayList<Integer>(size);
    Random random = new Random();
    for (int i  = 0; i < size; i++){      
      newList.add(random.nextInt(maxval));

      //old: newList[i] = 
      //new: newList.get(i) = 

      //What goes in the parenthesis is the value that we want added: -- no equals
      //newList.add(random.nextInt(maxval));
    }
    //System.out.println
    return newList;
  }

  /**
  Parameters:
  - dataList - an ArrayList of integer values.
  Returns:
  - The sum of all of the elements of the ArrayList.
  */
  public static int sumOfList(ArrayList<Integer> dataList){
    int sum = 0;
    for (int i  = 0; i < dataList.size(); i++){      
      sum = sum + dataList.get(i);
  }
    return sum;//placeholder to compile.
  }
  /**
  Parameters:
  - dataList - an ArrayList of Integers
  - index1, index2 - the two locations to swap.
  Preconditions:
  - index1 and index2 are valid indecies of dataList
  Postconditions:
  - The ArrayList is modified such that
    The value that was in dataList[index1] is now in dataList[index2], and
    the value  that was in dataList[index2] is now in dataList[index1].
  - No other values should be modified.
  */
  public static void swapElements(ArrayList<Integer> dataList, int index1,int index2){
    int temp = dataList.get(index1);
    int temp2 = dataList.get(index2);

    dataList.add(index1,temp2);
    dataList.add(index2,temp);

  }

  /**
  Parameters:
  - dataList - an AraryList of Integers
  - valueToRemove - the value to remove
  Postconditions:
  - The dataList is modified such that all occurances of valueToRemove are removed.
  */
  public static void removeValue(ArrayList<Integer> dataList, int valueToRemove){
      for (int i=dataList.size()-1; i>0; i--) {
        if (dataList.get(i) == valueToRemove) {
          dataList.remove(i);
      }
    }
  }


  /**
  Parameters:
  - ListA,ListB - ArrayLists of integer values.
  Preconditions:
  - ListA and ListB have equal lengths.
  Returns:
  - A new ArrayList that contains the sum of the corresponding indecies of the two arraylists.
    e.g. sumLists( [1,2,3], [4,0,5]) would return: [5,2,8]
  Postconditions:
  - The parameter ArrayLists should not be modified.
  */
  public static ArrayList<Integer>sumLists(ArrayList<Integer>ListA,ArrayList<Integer>ListB){
   
    ArrayList <Integer> sumArrays = new ArrayList <Integer>(ListA.size());

    for (int i=0; i<ListA.size(); i++) {
      int sum = ListA.get(i) + ListB.get(i);
      sumArrays.add(i,sum);
    }
    return sumArrays;
  }

  /** zipLists
  Parameters:
  - ListA,ListB - ArrayLists of integer values.
  Returns:
  - A new ArrayList that contains all of the elements from both ArrayLists in alternating order starting with ListA's first element.
    When one list has no more values to add, continue adding the remaining values of the longer list.
    e.g. zipLists( [1,2,3,4], [8,9]) would return: [1,8,2,9,3,4]
  Postconditions:
  - The parameter ArrayLists should not be modified.
  */
  public static ArrayList<Integer> zipLists(ArrayList<Integer>ListA,ArrayList<Integer>ListB){
       ArrayList <Integer> zipList = new ArrayList <Integer>(ListA.size()*2);

    for (int i=0; i<ListA.size(); i++) {
      for (int j=0; i<ListB.size(); i++){
        zipList.add(i,ListA.get(i));
        zipList.add(2*i,ListB.get(j));
      }
        
      }
    
    return zipList;//placeholder to compile.
  }



  //buildRandomList(5,10)
  public static void main(String[] args) {

    ArrayList<Integer> al;
   

    //Uncomment these to test buildRandomList
    al = buildRandomList(10,100);
    System.out.println(al);
    System.out.println("Sum of List");
    System.out.println(sumOfList(al));
    //Uncomment these to test swapElements
    swapElements(al,2,6); // NOTE: had to include al
    System.out.println(al);

    // Uncomment these to test removeValue
    al.add(5);
    al.set(2,5);
    System.out.println(al); // needed al, not a
    removeValue(al,5);
    System.out.println(al); // needed al, not a

    ArrayList<Integer> alist;
    ArrayList<Integer> blist;
    alist = buildRandomList(5,70);
    blist = buildRandomList(2,70);

    System.out.println(alist);
    System.out.println(blist);
    System.out.println("Zip List");
    System.out.println(zipLists(alist,blist));
  }

} 
```
