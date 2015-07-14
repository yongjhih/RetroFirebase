# RetroFirebase

Before:

```java
Firebase ref = new Firebase("https://docs-examples.firebaseio.com/android/saving-data/fireblog");
```

```java
public class User {
    private int birthYear;
    private String fullName;

    public User() {}

    public User(String fullName, int birthYear) {
        this.fullName = fullName;
        this.birthYear = birthYear;
    }

    public long getBirthYear() {
        return birthYear;
    }

    public String getFullName() {
        return fullName;
    }
}

Firebase alanRef = ref.child("users").child("alanisawesome");

User alan = new User("Alan Turing", 1912);

alanRef.setValue(alan);
```

```java
//Referencing the child node using a .child() on it's parent node
alansRef.child("fullName").setValue("Alan Turing");
alansRef.child("birthYear").setValue(1912);
```
