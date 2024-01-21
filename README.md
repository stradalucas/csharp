## C# 6 CARACTERUSTUCAS

### 1. String Interpolation
```
string name = "Jonh";
int age = 30;
string result = $"{name} is {age} year old."
```

### 2. Null Conditional Operator
```
string result = (person != null && person.Address != null) 
                ? person.Address.City 
                : null;
                
string result = person?.Address?.City;
```

### 3. Null-Coalescing Operator
```
int result = nullableValue ?? 10;
```

### 4. Auto-Implemented Properties
```
public class Person
 {
    private string  name;

    public string Name {
        get { return name; }
        set { name = value }
    }
 }
```
```
public class Person {
    public string name {get; set;}
    public string name {get; set;} = "Diman";
}
```

### 5. Expression-Bodied

```
public class Person
 {
      private int age;
      private int Age 
      {
          get { return age; }
          set { age = value >= 0 ? value : 0 }
      }
  
      public void IncrementAge()
      {
          Age++;
      }
 }
```
```
public class Person
{
    private int age;
    private int Age 
    {
        get => age;
        set => age = value >= 0 ? value : 0 
    }
    public void IncrementAge() => Age++;
}
```

### 6. Collection Initializer

```
List<Person> people = new List<Person>();
people.Add(new Person {Name = "Alice", Age = 25});
people.Add(new Person {Name = "Bod", Age = 30});
people.Add(new Person {Name = "Charlie", Age = 22});
```
```
List<Person> people = new List<Person>
{
    new Person {Name = "Alice", Age = 25};
    new Person {Name = "Bod", Age = 30};
    new Person {Name = "Charlie", Age = 22};
}
```

### 7. Static Using Statement
```
public static class MathOperations 
{
    public static int Add(int a, int b) => a + b; 
    public static int Substract(int a , int b) => a - b;
}

class Program 
{
    using static MathOperations;

    static void Main()
    {
        int sum = Add(5, 3);
        int difference = Substract(13, 7);
    }
}
```
