Quicksort ist ein schneller Sortieralgorithmus, der eine Liste durch wiederholte Aufteilung und Sortierung in Teillisten organisiert. Dabei wird ein [[Pivot-Element]] ausgewählt, die Liste in Elemente kleiner und größer als das Pivot geteilt, und dieser Prozess wird [[rekursiv]] wiederholt, bis die gesamte Liste sortiert ist.

Beispiel in c#
#quicksort_csharp
```csharp
using System;

class QuickSortExample
{
    static void Main()
    {
        int[] array = { 5, 2, 9, 1, 5, 6 };
        
        Console.WriteLine("Unsorted Array:");
        PrintArray(array);

        QuickSort(array, 0, array.Length - 1);

        Console.WriteLine("\nSorted Array:");
        PrintArray(array);
    }

    static void QuickSort(int[] array, int low, int high)
    {
        if (low < high)
        {
            int pivotIndex = Partition(array, low, high);

            QuickSort(array, low, pivotIndex - 1);
            QuickSort(array, pivotIndex + 1, high);
        }
    }

    static int Partition(int[] array, int low, int high)
    {
        int pivot = array[high];
        int i = low - 1;

        for (int j = low; j < high; j++)
        {
            if (array[j] < pivot)
            {
                i++;
                Swap(array, i, j);
            }
        }

        Swap(array, i + 1, high);
        return i + 1;
    }

    static void Swap(int[] array, int i, int j)
    {
        int temp = array[i];
        array[i] = array[j];
        array[j] = temp;
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

python:
#quicksort_python
```python
def quicksort(array):
    if len(array) <= 1:
        return array
    else:
        pivot = array[0]
        less = [x for x in array[1:] if x <= pivot]
        greater = [x for x in array[1:] if x > pivot]
        return quicksort(less) + [pivot] + quicksort(greater)

# Beispiel
unsorted_array = [5, 2, 9, 1, 5, 6]

print("Unsorted Array:")
print(unsorted_array)

sorted_array = quicksort(unsorted_array)

print("\nSorted Array:")
print(sorted_array)

```