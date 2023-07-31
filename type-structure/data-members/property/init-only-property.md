# Init-Only property

#### When

* value is set by outside only when object is initialized

#### How

```csharp
public class User 
{
    private string _firstName; 
    
    public string FirstName { get => _firstName; init => _firstName = value;
}
```
