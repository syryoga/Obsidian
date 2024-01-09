In C# werden Bedingungen und Schleifen verwendet, um den Programmfluss zu steuern und repetitive Aufgaben zu automatisieren. Hier sind einige grundlegende Beispiele:

### Bedingungen:

1. **if-Anweisung:** #if_schleife_csharp
   ```csharp
   int number = 10;
   if (number > 0)
   {
       Console.WriteLine("Die Zahl ist positiv.");
   }
   else if (number == 0)
   {
       Console.WriteLine("Die Zahl ist null.");
   }
   else
   {
       Console.WriteLine("Die Zahl ist negativ.");
   }
   ```

2. **switch-Anweisung:**
   ```csharp
   int dayOfWeek = 3;
   switch (dayOfWeek)
   {
       case 1:
           Console.WriteLine("Montag");
           break;
       case 2:
           Console.WriteLine("Dienstag");
           break;
       // ... Weitere Fälle ...
       default:
           Console.WriteLine("Ungültiger Tag");
           break;
   }
   ```

### Schleifen:

1. **for-Schleife:**
   ```csharp
   for (int i = 0; i < 5; i++)
   {
       Console.WriteLine($"Schleifenindex: {i}");
   }
   ```

2. **while-Schleife:**
   ```csharp
   int counter = 0;
   while (counter < 3)
   {
       Console.WriteLine($"Schleifenindex: {counter}");
       counter++;
   }
   ```

3. **do-while-Schleife:**
   ```csharp
   int number;
   do
   {
       Console.WriteLine("Bitte gib eine positive Zahl ein: ");
   } while (!int.TryParse(Console.ReadLine(), out number) || number <= 0);
   ```

Diese Bedingungen und Schleifen ermöglichen es, unterschiedliche Pfade im Programmfluss zu wählen und wiederholte Aktionen auszuführen. Beachte, dass die Kommentare und Variablennamen in Englisch gehalten sind, wie von dir gewünscht.

In C# gibt es auch die `foreach`-Schleife, die speziell für die Iteration über Elemente in einer Sammlung, wie Arrays oder Listen, entwickelt wurde. Hier ist ein Beispiel:

```csharp
string[] colors = { "Rot", "Grün", "Blau" };

// Iteration über jedes Element in einem Array
foreach (string color in colors)
{
    Console.WriteLine(color);
}
```

In diesem Beispiel wird die `foreach`-Schleife verwendet, um jedes Element im Array `colors` zu durchlaufen und es auf der Konsole auszugeben. Du kannst die `foreach`-Schleife auch für andere Sammlungstypen verwenden, wie z. B. Listen:

```csharp
List<int> numbers = new List<int> { 1, 2, 3, 4, 5 };

// Iteration über jedes Element in einer Liste
foreach (int number in numbers)
{
    Console.WriteLine(number);
}
```

Die `foreach`-Schleife vereinfacht die Iteration über die Elemente einer Sammlung und ist besonders nützlich, wenn du nicht die genauen Indizes der Elemente kennen musst.