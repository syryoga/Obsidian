#recursiv
Rekursiv bezieht sich auf einen Prozess, bei dem eine Funktion oder ein Algorithmus sich selbst aufruft, um ein Problem in kleinere Teilprobleme zu zerlegen und deren Lösungen zu kombinieren.

Beispiel c#: #recursive_methode_csharp
```csharp
using System;

class Program
{
    static void Main()
    {
        int n = 10; // Anzahl der Fibonacci-Zahlen, die berechnet werden sollen
        Console.WriteLine($"Die ersten {n} Fibonacci-Zahlen sind:");
        
        for (int i = 0; i < n; i++)
        {
            Console.Write(Fibonacci(i) + " ");
        }
    }

    static int Fibonacci(int n)
    {
        if (n <= 1)
        {
            return n;
        }
        else
        {
            return Fibonacci(n - 1) + Fibonacci(n - 2);
        }
    }
}

```

Beispiel python: #recursive_methode_python  #fibonacci
```python
def fibonacci(n):
    if n <= 1:
        return n
    else:
        return fibonacci(n - 1) + fibonacci(n - 2)

# Anzahl der Fibonacci-Zahlen, die berechnet werden sollen
n = 10
print(f"Die ersten {n} Fibonacci-Zahlen sind:")
for i in range(n):
    print(fibonacci(i), end=" ")

```