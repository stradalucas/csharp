## Switch expressions.

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
