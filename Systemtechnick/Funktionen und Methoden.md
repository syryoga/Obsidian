In C# werden Funktionen und Methoden verwendet, um Code in abgeschlossene, wiederverwendbare Abschnitte zu strukturieren. Hier sind grundlegende Beispiele:

### Funktionen und Rückgabewerte:

```csharp
// Funktion mit einem Rückgabewert
int AddiereZahlen(int a, int b)
{
    return a + b;
}

// Funktion aufrufen und das Ergebnis verwenden
int summe = AddiereZahlen(3, 7);
Console.WriteLine($"Die Summe ist: {summe}");
```

### Methoden und Parameter:

```csharp
// Methode ohne Rückgabewert
void BegrüßeNutzer(string name)
{
    Console.WriteLine($"Hallo, {name}!");
}

// Methode aufrufen
BegrüßeNutzer("John");
```

### Überladene Methoden:

```csharp
// Überladene Methode mit unterschiedlichen Parametertypen
void ZeigeInfo(string text)
{
    Console.WriteLine($"Info: {text}");
}

void ZeigeInfo(int zahl)
{
    Console.WriteLine($"Info: {zahl}");
}

// Methoden aufrufen
ZeigeInfo("Dies ist ein Text.");
ZeigeInfo(42);
```

### Optionalen Parameter:

```csharp
// Methode mit optionalem Parameter
void DruckeNachricht(string nachricht, bool druckeZeit = true)
{
    if (druckeZeit)
    {
        Console.WriteLine($"{DateTime.Now}: {nachricht}");
    }
    else
    {
        Console.WriteLine(nachricht);
    }
}

// Methode aufrufen mit und ohne optionalen Parameter
DruckeNachricht("Hallo, Welt!");
DruckeNachricht("Guten Tag!", false);
```

### **Lambda-Ausdrücke:**
Lambda-Ausdrücke ermöglichen die Erstellung anonymer Funktionen, was besonders nützlich ist, wenn du kurzlebige Funktionen benötigst.

```csharp
// Lambda-Ausdruck für eine Funktion
Func<int, int, int> addiere = (a, b) => a + b;

int summe = addiere(3, 7);
Console.WriteLine($"Die Summe ist: {summe}");
```

### **Rekursive Funktionen:**
Rekursion ist eine Technik, bei der eine Funktion sich selbst aufruft. Dies ist nützlich für bestimmte Arten von Problemen, insbesondere wenn sie eine iterative Lösung nicht so elegant unterstützen.

```csharp
// Rekursive Funktion für die Berechnung der Fakultät
int Fakultät(int n)
{
    if (n == 0 || n == 1)
        return 1;
    else
        return n * Fakultät(n - 1);
}

int result = Fakultät(5);
Console.WriteLine($"Die Fakultät von 5 ist: {result}");
```

### **Erweiterungsmethoden:**
Erweiterungsmethoden ermöglichen es, bestehenden Klassen neue Methoden hinzuzufügen, ohne den Quellcode der Klasse selbst zu ändern.

```csharp
// Erweiterungsmethode für die String-Klasse
public static class StringExtensions
{
    public static bool IstPalindrom(this string text)
    {
        // Überprüfe, ob der Text ein Palindrom ist
        // (Beispiel: "Anna" ist ein Palindrom)
        // Implementierung hier...
    }
}

// Verwendung der Erweiterungsmethode
string wort = "Anna";
bool istPalindrom = wort.IstPalindrom();
Console.WriteLine($"Ist ein Palindrom: {istPalindrom}");
```

### **Delegaten und Ereignisse:**
Delegaten ermöglichen es, Funktionen als Parameter zu übergeben oder als Rückgabewert zu haben. Ereignisse sind eine besondere Art von Delegaten, die verwendet werden, um auf Änderungen in einem Objekt zu reagieren.

```csharp
// Delegat für eine Funktion mit zwei int-Parametern und einem int-Rückgabewert
public delegate int MathematischeOperation(int a, int b);

// Ereignis, das auftritt, wenn eine MathematischeOperation ausgeführt wird
public event MathematischeOperation MathOperationAusgeführt;

// Beispielaufruf des Ereignisses
int ergebnis = MathOperationAusgeführt?.Invoke(5, 3) ?? 0;
Console.WriteLine($"Ergebnis der Mathematischen Operation: {ergebnis}");
```

Diese zusätzlichen Konzepte erweitern die Möglichkeiten von Funktionen und Methoden in C# und bieten mehr Flexibilität und Funktionalität je nach den Anforderungen deines Codes.