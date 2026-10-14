# RANDOM NUMBER GENERATION

`Math.random()` - [0, 1)

Roll a 12 sided die [1, 12]

```java
int roll = (int) (Math.random() * 12) + 1;
````

```java
int val = (int) (Math.random() * numValues) + start;
```

where `numValues = end - start + 1`

# MATH AND CASTING

casting:
```java
(int) 1.3 -> 1
(int) 1.7 -> 1
```

rounding:
```java
1.3 -> (int) (1.3 + 0.5)
1.7 -> (int) (1.7 + 0.5)
-2.3 -> (int) (-2.3 - 0.5)
```

# METHODS

Two types:
- Class methods (`static`)
- Instance methods (no `static`)

Technically constructors are special, but are similar to method.
Key difference: Constructors have no return type and are always named after the class.

## CLASS METHODS

Declared as static.

Called on the class itself.

For example, we do `Math.random()` instead of using a `Math m` object.

Key idea: Cannot refer to individual values or instance variables, they are not called on an object. Can only use general values and methods shared by the entire class. (An example is how `Math` shares `Math.PI`).

## INSTANCE METHODS

Called on objects (reference-type variables).

This allows us to access specific data about an individual instance (copy) of the class (blueprint).

## METHOD SIGNATURES

These must be unique.

They are the name of the method, followed by the order of the parameter types. 

Parameter names and return type do not change the signature.

## RETURN TYPES

What the method is expected to return.

You must always return a value of that type.

If you don't want to return something, put `void`.

The `return` statement acts as an exit ramp (immediately ends the method call).

# OBJECTS

To create a Dog object (formally called instantiation):

```java
Dog d = new Dog("Spot");
```

where the Dog class has a constructor that takes a `String` parameter.

# ENCAPSULATION

Discussion behind `public` and `private`.

Key idea: A object should control its own data. It specifies the behaviors (methods) that other classes can use to interact with said data.

Instance variables are `private` (controlled by the object itself).

Constructors and methods are `public` because they are mainly used by other classes.