# Parameters

#### In parameter

* used to pass a read-only parameter
* method can read the value, but can't modify

```csharp
public int DoSomething(in int value)
{
    var result = value;
    // value = 20; // invalid
    return result;
}

// call
var value = 10;
DoSomething(value);
```



#### Out parameter

* used to pass parameter to the method for output purposes
* method required to assign a value to the parameter before it returns

```csharp
public void DoSomething(out int value)
{
    // return value // invalid
    value = 10;
}

DoSomething(out var value);
```



#### Ref parameter

* used to pass a parameter by reference

```csharp
public void DoSomething(ref int value)
{
    value = 10; // actual value in passed variable is changed
}

var value = 1;
DoSomething(ref value);
```



#### Params parameter

* used to pass variable number of arguments of the same type

```csharp
public void DoSomething(params int[] values)
{
    foreach(var value in values)
    {
        // processing values    
    }
}
```

####

#### Optional parameter

* used to have optional input values in method

```csharp
public void DoSomething(int valueA, int valueB = 10)
{
    // do something
}

DoSomething(10);
DoSomething(10, 20);
```



#### Named parameter

* allow to pass arguments by specifying parameter name explicitly

```csharp
public void DoSomething(int valueA, int valueB)
{
    // do something
}

DoSomething(valueB: 10, valueA: 20);
```



