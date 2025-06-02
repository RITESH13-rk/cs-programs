using System;

class BubbleSortExample
{
    static void Main()
    {
        int[] arr = { 45, 12, 78, 23, 56, 10 };
        int n = arr.Length;

        Console.WriteLine("Original array:");
        PrintArray(arr);

        // Bubble Sort Algorithm
        for (int i = 0; i < n - 1; i++)
        {
            for (int j = 0; j < n - i - 1; j++)
            {
                if (arr[j] > arr[j + 1])
                {
                    // Swap arr[j] and arr[j + 1]
                    int temp = arr[j];
                    arr[j] = arr[j + 1];
                    arr[j + 1] = temp;
                }
            }
        }

        Console.WriteLine("\nSorted array using Bubble Sort:");
        PrintArray(arr);
    }

    static void PrintArray(int[] array)
    {
        foreach (int item in array)
        {
            Console.Write(item + " ");
        }
        Console.WriteLine();
    }
}
