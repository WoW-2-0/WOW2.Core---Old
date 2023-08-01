# Property



{% hint style="info" %}
Imagine a situation&#x20;
{% endhint %}







#### What





#### How



Property types



* Read-write - [Broken link](broken-reference "mention")
* Read-only property
* Write-only property
* Init-only property





#### When

* we have additional logic for `get` and `set` operations
* all data members need to be declared as property initially&#x20;





#### How

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

