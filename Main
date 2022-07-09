import java.util.ArrayList;
import java.util.Arrays;
import java.util.Collection;
import java.util.Collections;
import java.util.LinkedList;
import java.util.List;
import java.util.Random;
import java.util.Scanner;
/*
 * Program 4
 * ArrayList, Arrays, and LinkedLists
 * Cs 160-1
 * 03-13-2022
 * @author Conor Murphy
 */
public class GenMethods {
	public String getIdentificationString() {
		return "Program 4, Conor Murphy";
	}
	public static <E> ArrayList<E> removeDuplicates(ArrayList<E> list){
		/*Write the following method that returns a new ArrayList. The 
		new list contains the nonduplicate (i.e., distinct) elements from the original list.*/
		ArrayList<E> newList = new ArrayList<E>();
		for(int i = 0; i<list.size(); i++) {
			if(!newList.contains(list.get(i))) {
				newList.add(list.get(i));
			}
		}
		//removes duplicates from ArrayList and adds it to newList
		return newList;
	}
	public static <E> void shuffle(ArrayList<E> list) {
		Random rand = new Random(340L);
		int randElement1;
		int randElement2;
		E temp;
		for(int i = 0; i<30; i++) {
			randElement1 = rand.nextInt(list.size());
			randElement2 = rand.nextInt(list.size());
			temp = list.get(randElement1);
			list.set(randElement1, list.get(randElement2));
			list.set(randElement2, temp);
			//swap element in arrayList
		}
	}
	public static <E extends Comparable<E>> E max(ArrayList<E> list) {
		//Write the following method that returns the largest element in an ArrayList:
		Collections.sort(list);
		//sorts list using collection
		return list.get(list.size()-1);//return last element of list
		
	}
	public static <E extends Comparable<E>> int linearSearch(E[] list, E key) {
		for(int i = 0; i< list.length; i++) {
			if (list[i].compareTo(key) == 0) {
				return i;
				//return element that key was found at
			}
		}
		return -1;
		//if it doesn't find key, it return -1

	}
	public static <E extends Comparable<E>> E max(E[] list) {
		//Implement the following method that returns the maximum element in an array:
		E maxNum = list[0];
		for (int i = 1; i< list.length; i++) {
			if(list[i].compareTo(maxNum)>0) {
				maxNum = list[i];
			}
		}	
		return maxNum;
	}
	public static <E extends Comparable<E>> E max(E[][] list) {
		//Implement a generic method that returns the maximum element in a two-dimensional array.
		E maxValue = list[0][0];
		for(int i = 0; i< list.length; i++) {
			for(int j = 0; j< list[i].length; j++) {
				if (list[i][j].compareTo(maxValue) >0) {
					maxValue = list[i][j];
				}
			}
		}
		return maxValue;
		
	}
	public static void main(String[] args) {
		//Read in a number n that represents the number of elements in the lists.
		Scanner scnr = new Scanner(System.in);
		 int n = scnr.nextInt();

		/*Read in n elements to initialize and fill an array of Integers named 'list' 
		 while simultaneously initializing a linked list of Integers named 'linked' 
		 from the same input.*/
		 Integer[] list = new Integer[n];
		 LinkedList<Integer> linked = new LinkedList<Integer>();//creates linked List
		 for(int i = 0; i< n; i++) {
			 list[i] = scnr.nextInt();
			 linked.add(list[i]);//adds list element to linkedList
		 }
 
		//Print 'list'. (use Arrays.toString(array))
		 System.out.println(Arrays.toString(list));
		 

		//Print 'linked' (just put 'linked' into print statement)
		 System.out.println(linked);

		//Read in k key value to search for in list.
		 int k = scnr.nextInt();

		//Call linearSearch(list, k) and print the result: Key k was found at position
		 //result, or Key k was not found
		 int result = linearSearch(list, k);
		 if (result == -1) {
			 System.out.println("Key " + k + " was not found");
		 }
		 else {
			 System.out.println("Key " + k + " was found at position"+ result);
		 }

		//Call max(list) and print the result: 'Result' is the max element*/
		System.out.println(max(list) + " is the max element");
		
		

		//Read in an integer m for first dimension of a 2-D array.
		int m = scnr.nextInt();

		//Read in an integer p for second dimension of a 2-D array.
		int p = scnr.nextInt();

		//Initialize a 2-D array using m and p named 'list2'
		Integer[][] list2 = new Integer[m][p];

		//Read in m x p elements to fill 'list2'.
		for(int i = 0; i< list2.length; i++) {
			for(int j = 0; j<list2[i].length; j++) {
				list2[i][j] = scnr.nextInt();
			}
		}

		/*Print 'list2'. You can not just use a single print statement, 
		 * but will instead need to implement nested for loops. 
		 * (Format: rows of data on separate lines with a space in between each data)
		Example:
		1 2 3 4 
		2 3 4 5
		3 4 5 6*/
		for(int i = 0; i< list2.length; i++) {
			for(int j = 0; j<list2[i].length; j++) {
				System.out.print(list2[i][j]+ " ");
			}
			System.out.println();
		}

		//Call max(list2) and print the result: 'Result' is the max element
		System.out.println(max(list2) + " is the max element");

		//Instantiate an ArrayList of type Integer named 'alist' from 'linked' 
		//(meaning 'alist' is a copy of 'linked')
		ArrayList<Integer> alist = new ArrayList<Integer>(linked);

		//Print out 'alist' using System.out.println(alist);
		System.out.println(alist);

		//Call removeDuplicates using 'alist' as the parameter
		ArrayList<Integer> newArray = removeDuplicates(alist);

		//Print the now unique 'alist' using System.out.println(alist);
		System.out.println(newArray);
		//Call shuffle using 'alist' as the parameter.
		shuffle(newArray);

		//Print 'alist' again using System.out.println(alist);
		System.out.println(newArray);

		//Find the max element of 'alist' and print: 'Result' is the max element*/
		System.out.println(max(newArray) + " is the max element");
		scnr.close();
	}
	}
