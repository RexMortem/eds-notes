# Lecture 15 - Generics

Notes on paper; not too detailed tbh but copy them over at some point if you want 
```Java
// Use this editor to write, compile and run your Java code online

class Box<E> { // E is by convention the type for an element 
    private E containedObject;
    
    public Box(E object){
        containedObject = object;
    }
    
    public void Set(E object){
        containedObject = object;
    }
    
    public E Get(){
        return this.containedObject;
    }
}

class KeyValuePair<K,V> {
    private final K Key;
    private V Value;
    
    public KeyValuePair(K Key, V Value){
        this.Key = Key;
        this.Value = Value;
    }
    
    public K GetKey(){
        return this.Key;
    }
    
    public V GetValue(){
        return this.Value;
    }
    public void SetValue(V NewValue){
        this.Value = NewValue;
    }
    
    public String toString(){
        return "This KeyValuePair has a key of: " + this.Key.toString() + " and a value of: " + this.Value.toString();
    }
}

class Util { // placing <K, V> causes an error as the static method needs to use it without needing an instance of the class
    public static<K,V> boolean equals(KeyValuePair<K,V> a, KeyValuePair<K,V> b){
        return (a.GetKey() == b.GetKey()) && (a.GetValue() == b.GetValue());
    } // place <K, V> at method level (need it so that it can work generically); for some reason it must be before the return type
}

class NumericalMethods {
    public static <T extends Number> boolean equals(T a, T b){
        return (a == b);
    }
    
    public static <T> T sum(T a, T b){ // this errors; look at it later
        return (a + b);
    }
}

class HelloWorld {
    public static void main(String[] args) {
        Box<Integer> anIntegerBox = new Box(5);
        System.out.println(anIntegerBox.Get());
        
        KeyValuePair<String, Integer> nameBalanceMapping = new KeyValuePair("Greg", 15);
        
        System.out.println(Util.equals(nameBalanceMapping, nameBalanceMapping));
    }
}
```