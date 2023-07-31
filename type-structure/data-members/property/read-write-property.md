# Read-Write property

#### When

* we have additional logic for `get` and `set` operations
* all data members need to be declared as property initially&#x20;





* includes 2 types of properties - auto-property and standard read-write property
* auto-property - underlying field will be created automatically and bind to **get** and **set** methods
* standard read-write property - underlying field must be created manually&#x20;

```csharp
public class User
{
    // auto property
    public string FirstName { get; set; }
    
    // standard read-write property
    private string _lastName;
    
    public string LastName { get => _lastName; set => _lastName = value; }
}
```

