# Generics
if code has been compiled there should be no exceptions in runtime, generics ensure type-safety

```Java
Integer i = 215;
Class<Integer> class = i.getClass(); // compile error
```

## Type erasure
Generics exist only in source code and are erasured on compilation (or casts or generate bridge methods).
```Java
public class Person implements Comparable<Person> {
  private String name;
  
  // Compile error: both methods have same erasure
  
  @Override
  public int compareTo(Person o) {
    return name.compareTo(o.name);
  }
  
  public int compareTo(Object o) {
    return toString().compareTo(o.ToString());
  }
}
```
Generics are erasured into `Object`. 

Type erasure example:

1. Before
```Java
class Holder<T> {
  private T value;

  public Holder(T t) {
    this.value = t;
  }

  public T get() {
    return value;
  }
}
```
2. After
```Java
class Holder {
  private Object value;

  public Holder(Object t) {
    this.value = t;
  }

  public Object get() {
    return value;
  }
}
```

So the code:
```Java
Holder<Integer> holder = new Holder<>(10);
Integer integer = holder.get();
```
After erasion during compilation looks like this:
```Java
Holder older = new Holder(10);
Integer integer = (Integer) holder.get(); // uses casting
```

## PECS
If a parameterized type represents a `T` producer, use `<? extends T>`. If it represents a `T` consumer, use `<? super T>`.
```Java
public static <T> T max(Collection<? extends T> coll, Comparator<? super T> comp)
```

