# Read-Only property



#### When

* underlying field is readonly
* value should not be updated by outside



#### How

* includes read-only property and expression-bodied read-only property
* &#x20;expression-bodied read-only property doesn't have `get` method

```csharp
public class User
{
    // read-only property
    private string _firstName;
    
    public string FirstName { get => _firstName; }
    
    // expression-bodied read-only property 
    public string _lastName;
    
    public string LastName => _lastName;
}
```

