## Switch expressions

```
public static string GetWorkTime (DayOfWeek dayOfWeek) => 
    dayOfWeek switch 
    {
        DayOfWeek.Monday => "9-5",
        DayOfWeek.Tuesday => "10-3",
        DayOfWeek.Wednesday => "10-3",
        DayOfWeek.Thursday => "10-3",
        DayOfWeek.Friday => "9-12",
        _ => ""
    }
```

## Range[..]

```
//Readble and slower
public static List<Product> TakeRangeMethod ()  
{
    var products = GetProducts();
    products = product.Skip(1).Take(3).ToList();
    return products;
}
```
```
//Shorter and faster
public static List<Product> TakeRangeMethod ()  
{
    var products = GetProducts();
    products = product.Take(1..4).ToList();
    return products;
}
```
