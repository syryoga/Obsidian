In der objektorientierten Programmierung (OOP) werden Programme durch die Organisation von Code in Objekten strukturiert. Hier sind einige wichtige Themen der OOP in C#:

### 1. **[[Klassen]] und Objekte:**
- **Klassen:** Eine Klasse ist eine Bauplan für Objekte. Sie definiert die Struktur und das Verhalten von Objekten.
  ```csharp
  public class Auto
  {
      public string Marke { get; set; }
      public int Baujahr { get; set; }

      public void Starten()
      {
          Console.WriteLine("Das Auto startet.");
      }
  }
  ```

- **Objekte:** Ein Objekt ist eine Instanz einer Klasse. Es verkörpert die Eigenschaften und Methoden, die in der Klasse definiert sind.
  ```csharp
  Auto meinAuto = new Auto();
  meinAuto.Marke = "BMW";
  meinAuto.Baujahr = 2022;
  meinAuto.Starten();
  ```

### 2. **Vererbung:**
Vererbung ermöglicht es einer Klasse, Eigenschaften und Methoden von einer anderen Klasse zu erben. Dies fördert die Wiederverwendbarkeit von Code.
```csharp
public class Elektroauto : Auto
{
    public bool HatElektromotor { get; set; }
    
    public void Aufladen()
    {
        Console.WriteLine("Das Elektroauto wird aufgeladen.");
    }
}
```

### 3. **Polymorphismus:**
Polymorphismus erlaubt es, dass Objekte einer abgeleiteten Klasse wie Objekte ihrer Basisklasse behandelt werden können.
```csharp
Auto meinElektroauto = new Elektroauto();
meinElektroauto.Starten(); // Verwendet die Starten-Methode der abgeleiteten Klasse (Elektroauto)
```

### 4. **Encapsulation (Kapselung):**
Kapselung verbirgt die internen Details einer Klasse vor externem Zugriff. Dies fördert die Sicherheit und erleichtert die Wartung.
```csharp
public class Bankkonto
{
    private decimal kontostand;

    public void Einzahlen(decimal betrag)
    {
        kontostand += betrag;
    }

    public decimal KontostandAbrufen()
    {
        return kontostand;
    }
}
```

### 5. **Abstrakte Klassen und Schnittstellen:**
Abstrakte Klassen und Schnittstellen bieten Mechanismen zur Definition von allgemeinen Funktionen, die von abgeleiteten Klassen implementiert werden müssen.
```csharp
// Abstrakte Klasse
public abstract class Figur
{
    public abstract double BerechneFläche();
}

// Schnittstelle
public interface IZeichnbar
{
    void Zeichnen();
}
```

Diese OOP-Konzepte ermöglichen eine modulare und strukturierte Programmierung, indem sie den Code in wiederverwendbare Einheiten organisieren. Vererbung, Polymorphismus und Kapselung sind besonders leistungsstarke Konzepte, die die Flexibilität und Wartbarkeit von Code verbessern.