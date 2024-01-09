#bubblesort
Bubblesort ist ein [[iterativ]]er Algorithmus, der die Elemente des Arrays nacheinander durchläuft und vergleicht. Wenn zwei benachbarte Elemente in der falschen Reihenfolge sind, werden sie vertauscht. Dieser Vorgang wird wiederholt, bis das Array sortiert ist.

Beispiel c#:
#bubblesort_csharp
```csharp
using System;

class BubbleSortExample
{
    static void Main()
    {
        int[] array = { 5, 2, 9, 1, 5, 6 };
        
        Console.WriteLine("Unsorted Array:");
        PrintArray(array);

        BubbleSort(array);

        Console.WriteLine("\nSorted Array:");
        PrintArray(array);
    }

    static void BubbleSort(int[] array)
    {
        int n = array.Length;

        for (int i = 0; i < n - 1; i++)
        {
            for (int j = 0; j < n - i - 1; j++)
            {
                if (array[j] > array[j + 1])
                {
                    // Vertausche die Elemente, wenn sie in der falschen Reihenfolge sind
                    int temp = array[j];
                    array[j] = array[j + 1];
                    array[j + 1] = temp;
                }
            }
        }
    }

    static void PrintArray(int[] array)
    {
        foreach (var element in array)
        {
            Console.Write(element + " ");
        }
        Console.WriteLine();
    }
}

```


Beispiel python:
#bubblesort_python
```python
def bubble_sort(array):
    n = len(array)

    for i in range(n):
        for j in range(0, n-i-1):
            if array[j] > array[j+1]:
                # Vertausche die Elemente, wenn sie in der falschen Reihenfolge sind
                array[j], array[j+1] = array[j+1], array[j]

# Beispiel
unsorted_array = [5, 2, 9, 1, 5, 6]

print("Unsorted Array:")
print(unsorted_array)

bubble_sort(unsorted_array)

print("\nSorted Array:")
print(unsorted_array)

```