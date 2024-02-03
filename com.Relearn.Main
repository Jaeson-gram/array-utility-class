package com.Relearn;

import java.util.Arrays;
import java.util.Random;

public class Main {

    public static void main(String[] args) {
	// write your code here
        //
        int[] firstArray = getRandomArray(10);
        System.out.println(Arrays.toString(firstArray));
        Arrays.sort(firstArray);
        System.out.println(Arrays.toString(firstArray));

        System.out.println("---".repeat(10));

        //the Array.fill()
        int[] secondArray = new int[10];
        System.out.println(Arrays.toString(secondArray));
        Arrays.fill(secondArray, 4);
        System.out.println(Arrays.toString(secondArray));

        //copying an array -> if you don't want to work on your original array
        System.out.println("---".repeat(10));
        int[] thirdArray = getRandomArray(10);
        System.out.println(Arrays.toString(thirdArray));

        int[] fourthArray = Arrays.copyOf(thirdArray, thirdArray.length);// ->for primitives,values get copied, for objects, references.
        System.out.println(Arrays.toString(fourthArray));

        Arrays.sort(fourthArray);
        System.out.println(Arrays.toString(thirdArray)); // -> doesn't affect the original at all
        System.out.println(Arrays.toString(fourthArray));

        System.out.println("---".repeat(10));

        int[] smallArray = Arrays.copyOf(thirdArray, 5); // -> Partial copy fourthArray is a full copy
        System.out.println(Arrays.toString(smallArray));

        int[] largeArray = Arrays.copyOf(thirdArray, 16);
        System.out.println(Arrays.toString(largeArray)); // -> copy plus additional elements

        //Searching using an interval search -> The Binary Search.
        String[] stringArray = new String[]{"Ajibola", "Justice", "Ada", "Uk", "Uzochukwu"};
        Arrays.sort(stringArray);
        System.out.println(Arrays.toString(stringArray));

        if (Arrays.binarySearch(stringArray, "Uzochukwu") >= 0)
            System.out.println("Uzochukwu Found!");

        System.out.println("---".repeat(10));
        //Testing for equality. Two arrays are equal if they have the same number of elements, and the same values in   each of those elements
        int[] In1 = new int[] {1, 2, 3, 4, 5};
        int[] In2 = new int[5];
        In2[0] = 1;
        In2[1] = 2;
        In2[2] = 3;
        In2[3] = 4;
        In2[4] = 5;

        if (Arrays.equals(In1, In2))
            System.out.println("The arrays In1 and In2 are equal!");
        else
            System.out.println("The arrays In1 and In2 are not equal!e");

        System.out.println("---".repeat(10));

        //CHALLENGE -> PRINT THE VALUES OF AN ARRAY IN REVERSE. SEE THE challengeForSortingInReverse() STATIC METHOD
        System.out.println("-".repeat(10) + " Challenge " + "-".repeat(10));
        System.out.println("---".repeat(10));

        int[] myChallengeArray = new int[10];

        challengeForSortingInReverse(myChallengeArray);

//        int[] challengeStore = challengeForSortingInReverse(myChallengeArray);
//        System.out.println(Arrays.toString(challengeStore)); -> The println statements make it too much to see, so we use what's above
    }

    private static int[] getRandomArray(int length) {
        int[] randomArray = new int[length];
        Random random =new Random();

        for (int i = 0; i < length; i++) {
            randomArray[i] = random.nextInt(101);
        }

        return randomArray;
    }

    //Challenge: Present an array reverse-sorted.
    private static int[] challengeForSortingInReverse(int[] array){
        //First things first: populate the array with random numbers...
        Random random = new Random();

        for (int i = 0; i < array.length; i++){
            array[i] = random.nextInt(101);
        }

        //copy the array to work with it
        int[] copiedArray = Arrays.copyOf(array, array.length);
        //printing before the reverse
        System.out.println("You array = " + Arrays.toString(copiedArray));

        //sort the array
        Arrays.sort(copiedArray);

        //create an int to target each element later
        int counter = array.length - 1;
        //for loop that does the job of assigning the reversed value to the array, now in ascending order, because the counter starts from the end
        for (int i = 0; i < array.length; i++){
            array[i] = copiedArray[counter];
            counter--;
        }

        //printing the values after sorting them, in reverse
        System.out.println("Your new array = " + Arrays.toString(array));

        //return
        return array;
    }
}
