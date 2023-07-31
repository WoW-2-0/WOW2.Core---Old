# Write-Only property



#### When

* setting part of data is allowed but actual data is not exposed

#### How

```csharp
public class User 
{
    private string _firstName; 
    
    public string FirstName { get => _firstName; init => _firstName = value;
}
```
