# rachel's page
## buggy Code for index traversing merge method:
```
      public ArrayList<Integer> merge(ArrayList<Integer> list1,
				    ArrayList<Integer> list2){
      
      ArrayList<Integer> mergedData = new ArrayList<Integer>();
      int counter1 = 0, counter2 = 0;

        // currently ONLY working if last element(s) in list2 are greater than last element(s) in list1
        
      while(mergedData.size()<list1.size()+list2.size()){
        if (counter1 < list1.size()){
          if (list1.get(counter1) < list2.get(counter2)){
            mergedData.add(list1.get(counter1));
            counter1++;
          } else {
            mergedData.add(list2.get(counter2));
            if(counter2 < list2.size()-1){
            counter2++;
            }
          }
        } else {
          mergedData.add(list2.get(counter2));
          counter2++;
        }
      }
      return mergedData;
    } 
```

## why this
### seriously why
![alt text](https://media.giphy.com/media/0Vv0Ne2CnOClIExIuL/giphy.gif "y tho")
