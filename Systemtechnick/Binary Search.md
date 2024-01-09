Der Algorithmus vergleicht das gesuchte Element mit dem Mittelwert der Liste und schließt die Hälfte der Liste aus, in der das Element nicht liegen kann. Dieser Prozess wird wiederholt, bis das Element gefunden wird oder die Liste keine verbleibenden Elemente hat.

In Stichworten:
- Nur auf sortierten Listen oder Arrays anwendbar.
- Vergleicht das gesuchte Element mit dem Mittelwert der Liste.
- Schließt die Hälfte der Liste aus, die das gesuchte Element nicht enthalten kann.
- Wiederholt diesen Prozess, bis das Element gefunden wird oder die Liste leer ist.

Die binäre Suche hat eine logarithmische Laufzeitkomplexität von O(log n), wobei "n" die Anzahl der Elemente in der Liste ist.

C# Beispiel: #binary_search_csharp
```csharp
using System;

class Program
{
    static void Main()
    {
        int[] sortedArray = { 1, 2, 3, 4, 5, 6, 7, 8, 9, 10 };
        int target = 7;

        int result = BinarySearch(sortedArray, target);

        if (result != -1)
        {
            Console.WriteLine($"Element {target} gefunden an Index {result}.");
        }
        else
        {
            Console.WriteLine($"Element {target} nicht gefunden.");
        }
    }

    static int BinarySearch(int[] array, int target)
    {
        int left = 0;
        int right = array.Length - 1;

        while (left <= right)
        {
            int mid = left + (right - left) / 2;

            if (array[mid] == target)
            {
                return mid; // Element gefunden, gibt den Index zurück
            }
            else if (array[mid] < target)
            {
                left = mid + 1;
            }
            else
            {
                right = mid - 1;
            }
        }

        return -1; // Element nicht gefunden
    }
}

```