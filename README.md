# Susie's portfolio
---
---


(![BE-Computer-Science](https://user-images.githubusercontent.com/46972076/180851562-9c072793-fcc4-4382-b16b-86eeff62a358.png)
)

## PROGRAMMING
### method to create play Nim
```

import java.io.*;
import java.util.*;

public class Nim
{
  public static void main( String[] args)
  {
    int stones = 12;
    int stonesTaken;
    Scanner in = new Scanner(System.in);
    //loop until game ends
    while(stones > 0 ){
      // prompt user for input : user taking turn
      System.out.println("Please enter a number from 1-3");
      stonesTaken = in.nextInt(); 
      in. nextLine();//taking from the user I
    
      // caculate the number of stones remaining.
      //print
      stones = stones - stonesTaken;
      System.out.println("There are " + stones + " left");
      //stones -= stonesTaken;
      
      //check for did I win??
      if(stones <= 0 )
      {
        System.out.println("You win!");
        
      }
        
      //machine turn
      System.out.println("Computers Turn");
      stonesTaken = (int)(Math.random()*3)+1;
      //Math.random()(max - min +1) + min
      stones = stones - stonesTaken;
      System.out.println("The Computer took " + stonesTaken);
      // caculate the number of stones remaining.
      //print
      System.out.println("There are " + stones + " left");
      //check for the win
      if(stones <= 0 )
      {
        System.out.println("Computer wins!");
        
      }
      
    }
  }
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
### Here is how to Code for index of
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
