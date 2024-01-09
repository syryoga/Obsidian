Ein Greedy-Algorithmus ist eine Entwurfsstrategie, bei der in jedem Schritt die lokal optimale Wahl getroffen wird, in der Hoffnung, dass dies zu einer global optimalen Lösung führt. Der Algorithmus wählt immer den besten verfügbaren Schritt, ohne den globalen Kontext zu berücksichtigen.

Charakteristiken eines Greedy-Algorithmus:

1. **Gierige Auswahl:** Der Algorithmus trifft in jedem Schritt die beste lokale Entscheidung.

2. **Lokal optimale Wahl:** Die getroffene Entscheidung scheint in diesem Schritt optimal zu sein.

3. **Hoffnung auf globale Optimierung:** Die Hoffnung besteht darin, dass durch die Kombination lokaler optimaler Entscheidungen eine globale optimale Lösung erreicht wird.

Beispiele für Greedy-Algorithmen:
- **Huffman-Codierung:** Minimierung der Gesamtlänge der Codewörter für eine gegebene Menge von Symbolen basierend auf ihrer Häufigkeit.
- **Prim's Algorithmus:** Finden eines minimalen Spannbaums in einem gewichteten Graphen.
- **Kruskal's Algorithmus:** Ebenfalls für die Konstruktion eines minimalen Spannbaums, jedoch auf eine andere Weise als Prim's Algorithmus.
- **Dijkstra's Algorithmus:** Finden des kürzesten Pfades von einem Startknoten zu allen anderen Knoten in einem gewichteten Graphen.

<span style="color:red">Es ist wichtig zu beachten, dass Greedy-Algorithmen nicht immer eine optimale Lösung garantieren, aber sie können in vielen Fällen effiziente Näherungslösungen liefern.</span>

C# Beispiel: #greedy_algorithmus_csharp
```csharp
using System;
using System.Collections.Generic;

class Program
{
    static void Main()
    {
        int[] coins = { 25, 10, 5, 1 };
        int amount = 63;

        List<int> result = GreedyCoinChange(coins, amount);

        Console.WriteLine($"Minimale Anzahl von Münzen: {result.Count}");
        Console.Write("Verwendete Münzen: ");
        Console.WriteLine(string.Join(", ", result));
    }

    static List<int> GreedyCoinChange(int[] coins, int amount)
    {
        List<int> result = new List<int>();

        Array.Sort(coins, (a, b) => b.CompareTo(a)); // Sortiere Münzen absteigend

        foreach (int coin in coins)
        {
            while (amount >= coin)
            {
                result.Add(coin);
                amount -= coin;
            }
        }

        return result;
    }
}

```
