# Java-LinkedList
The LinkedList class of the Java collections framework provides the functionality of the linked list data structure 
<img width="384" alt="linked" src="https://user-images.githubusercontent.com/83684733/152988452-0d28bc8a-825a-4996-88bd-0a8c6e48ef2c.png">
Java LinkedList
The LinkedList class of the Java collections framework provides the functionality of the linked list data structure 
 
	

Each element in a linked list is known as a node. It consists of 3 fields:
•	Prev - stores an address of the previous element in the list. It is null for the first element
•	Next - stores an address of the next element in the list. It is null for the last element
•	Data - stores the actual data

Creating a Java LinkedList
Here is how we can create linked lists in Java:
LinkedList<Type> linkedList = new LinkedList<>();

// create Integer type linked list
LinkedList<Integer> linkedList = new LinkedList<>();

// create String type linked list
LinkedList<String> linkedList = new LinkedList<>();
Example: Create LinkedList in Java
import java.util.LinkedList;

class Main {
  public static void main(String[] args){

    // create linkedlist
    LinkedList<String> animals = new LinkedList<>();

    // Add elements to LinkedList
    animals.add("Dog");
    animals.add("Cat");
    animals.add("Cow");
    System.out.println("LinkedList: " + animals);
  }
}

Output
LinkedList: [Dog, Cat, Cow]

Working of a Java LinkedList
 
Methods of Java LinkedList
Cursor:-
If we want to retrieve object one by one from the collection then we should go for cursor.
					Cursor
1]Enumerator            2]Iterator                 3]List Iterator

Iterator:-
#Universal cursor
#We can apply iterator concept for any collection object.
# By using Iterator we can perform both read and remove operation
#we can create Iterator object by using iterator () of collection interface
	Iterator Itr =C.Iterator();
Limitation:-
1]we can move only toward forward direction
2]Iterator can perform only read and remove operation and we cant perform replacement of new object .
Iterator<String> itr=list.iterator();
     while(itr.hasNext())
{
       System.out.println(itr.next());
}

Methods of LinkedList class:
LinkedList<String>
LinkedList<String> obj=new LinkedList<String>();
1]Add elements:-add()  , addFirst()   ,addLast(),  add(2,__)
	1]obj.add(“Hello”);  // It adds the item at the end of the list.
	2]obj.add(2,”name”); // It adds an item at the given index of the the list
3] LinkedList<String> llistobj = new LinkedList<String>();
ArrayList<String> arraylist= new ArrayList<String>();
arraylist.add("String1");
arraylist.add("String2");
llistobj.addAll(arraylist);
This piece of code would add all the elements of ArrayList to the LinkedList.
4]obj.addFirst(“   “);It adds the item (or element) at the first position in the list.
5]obj.addLast(“   “);It inserts the specified item at the end of the list.
6]obj.clear();It removes all the elements of a list.
7]cbj.clone(); // It returns the copy of the list.
Object str= obj.clone();
 System.out.println(str);
8]Boolean contain(Object item) //It checks whether the given item is present in the list or not. If the item is present then it returns true else false.
boolean var = obj.contains("TestString");
9]obj.get(2) //It returns the item of the specified index from the list.
10]obj.getFirst();It fetches the first item from the list.
11]obj.getLast();It fetches the last item from the list.
12]obj.indexof(“hello”);// It returns the index of the specified item.
13]obj.lastIndexOf(“ “)//integer variable pos will be having the index of last occurrence of string “hello”.
14]obj.poll()//It returns and removes the first item of the list.
Object o = obj.poll();
15]obj.pollFirst()//same as poll() method. Removes the first item of the list.
Object o = obj.pollFirst();
16]obj.pullLast()//It returns and removes the last element of the list.
Object o = obj.pollLast();
17]obj.remove()//It removes the first element of the list.
18] obj.remove(4)// It removes the item from the list which is present at the            
			Specified index.
19] obj.remove(“  hello  ”)//
20] obj.removeFirst( )
21] obj.removeLast( )
22]obj.removeFirstOccurance(“  text ”)
22]obj.removeLastOccurance(“  text ”)
23]obj.set(2,”test”)//  It updates the item of specified index with the give value.
24]obj.size();//It returns the number of elements of the list


)		       
 2]Access Elements:- get() , Iterator() ,listiterator()
3]Change Element:-set()
4]Remove Element:-remove()



import java.util.LinkedList;

class Main {
  public static void main(String[] args){
    // create linkedlist
    LinkedList<String> animals = new LinkedList<>();

    // add() method without the index parameter
    animals.add("Dog");
    animals.add("Cat");
    animals.add("Cow");
    System.out.println("LinkedList: " + animals);

    // add() method with the index parameter
    animals.add(1, "Horse");
    System.out.println("Updated LinkedList: " + animals);

   // get the element from the linked list
    String str = animals.get(1);
    System.out.print("Element at index 1: " + str);
  
   // change elements at index 2
    animals.set(2, "maniii");
    System.out.println("Updated LinkedList: " +animal);

   // remove elements from index 3
    String str = animals.remove(3);
    System.out.println("Removed Element: " + str);
System.out.println("Updated LinkedList: " +animals);


  }
}
Output
1]LinkedList: [Dog, Cat, Cow]
  Updated LinkedList: [Dog, Horse, Cat, Cow]
2]Accessed Element at index 1:Horse
3]Updated linked list:- : [Dog, Horse, manii, Cow]
4] Removed Element: cow
 New LinkedList: : [Dog, Horse, manii]


Other Methods
Methods	Description
contains()	checks if the LinkedList contains the element
indexOf()	returns the index of the first occurrence of the element
lastIndexOf()	returns the index of the last occurrence of the element
clear()	removes all the elements of the LinkedList
iterator()	returns an iterator to iterate over LinkedList

LinkedList as Deque and Queue
Methods	Descriptions
addFirst()	adds the specified element at the beginning of the linked list
addLast()	adds the specified element at the end of the linked list
getFirst()	returns the first element
getLast()	returns the last element
removeFirst()	removes the first element
removeLast()	removes the last element
peek()	returns the first element (head) of the linked list
poll()	returns and removes the first element from the linked list
offer()	adds the specified element at the end of the linked list
   
class Main {
  public static void main(String[] args)
{
     Queue<String> animals = new LinkedList<>();
     Deque<String> animals = new LinkedList<>();

    // add element at the beginning
    animals.add("Cow");
    System.out.println("LinkedList: " + animals);

LinkedList Vs. ArrayList
LinkedList	ArrayList
Implements List, Queue, and Deque interfaces.	Implements List interface.
Stores 3 values (previous address, data, and next address) in a single position.	Stores a single value in a single position.
Provides the doubly-linked list implementation.	Provides a resizable array implementation.
Whenever an element is added, prev and next address are changed.	Whenever an element is added, all elements after that position are shifted.
To access an element, we need to iterate from the beginning to the element.	Can randomly access elements using indexes.

Hierarchy of LinkedList class in Java
 

