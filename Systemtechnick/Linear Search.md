#lineare_suche #linear_search
Die lineare Suche ist ein Suchalgorithmus, der [[sequenziell]] jedes Element in einer Liste überprüft, um das gesuchte Element zu finden.

Beispiel c#: #linear_search_csharp
```csharp
using System;

class Program
{
    static void Main()
    {
        int[] array = { 4, 2, 7, 1, 9, 5 };
        int target = 7;

        int result = LinearSearch(array, target);

        if (result != -1)
        {
            Console.WriteLine($"Element {target} gefunden an Index {result}.");
        }
        else
        {
            Console.WriteLine($"Element {target} nicht gefunden.");
        }
    }

    static int LinearSearch(int[] array, int target)
    {
        for (int i = 0; i < array.Length; i++)
        {
            if (array[i] == target)
            {
                return i; // Element gefunden, gibt den Index zurück
            }
        }

        return -1; // Element nicht gefunden
    }
}

```

Python Beispiel: #linear_search_python
```python
def linear_search(array, target):
    for i, element in enumerate(array):
        if element == target:
            return i  # Element gefunden, gibt den Index zurück
    return -1  # Element nicht gefunden

array = [4, 2, 7, 1, 9, 5]
target = 7

result = linear_search(array, target)

if result != -1:
    print(f"Element {target} gefunden an Index {result}.")
else:
    print(f"Element {target} nicht gefunden.")

```

