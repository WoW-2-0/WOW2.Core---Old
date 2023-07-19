# Casting







#### When

* converting between similar data types



#### Why

* declarative conversion
* benefits from primitive type conversion

#### What

* process of converting one data type to another data type

#### How



Types of casting

* **Implicit Casting ( Widening )** &#x20;
  * conversion from smaller data type to larger one
  * no data or precision loss
  * automatically performed



* **Explicit Casting ( Narrowing )**
  * conversion from larger data type to smaller one
  * may have potential data loss
  * done by csting operator



**Usage**

* Implicit Casting

```csharp
int valueA = 10;
double valueB = valueA;
```

* Explicit casting

```csharp
double valueA = 10.567D;
int valueB = (int)valueA;
```



Side effects

**Boxing and Unboxing  -**&#x20;

**Boxing** - process of converting a value type to reference type and storing it in heap

```csharp
var valueA = 10;
var valueB = (object)valueA;
```

**Unboxing** - process of converting an object reference back to its original value type

```csharp
var valueA = (object)10;
var valueB = (int)valueA;
```











