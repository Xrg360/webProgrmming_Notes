
- **Class**: A blueprint for creating objects, containing properties (variables) and methods (functions).
  
  **Syntax:**
  ```php
  class ClassName {
      public $property;
      public function method() {
          // Code
      }
  }
  ```

- **Object**: An instance of a class, created using the `new` keyword.
  
  **Example:**
  ```php
  $car = new Car();
  $car->brand = "BMW";
  ```

---

## Key Concepts:

- **Constructor**: A special method (`__construct()`) that runs when an object is created to initialize properties.
  
  **Example:**
  ```php
  public function __construct($brand) {
      $this->brand = $brand;
  }
  ```

- **Access Modifiers**:
  - `public`: Accessible everywhere.
  - `private`: Accessible only within the class.
  - `protected`: Accessible within the class and subclasses.

- **Inheritance**: One class can inherit properties and methods from another using `extends`.

- **Static**: Methods/properties can be accessed without creating an object using `ClassName::method()`.

### String comparisons

### 1. **Equality Operators**:
- == : Compares strings for equality, ignoring type.
- === : Compares both value and type.

```php
$str1 = "Hello";
$str2 = "hello";

if ($str1 == $str2) { echo "Equal"; }    // False (case-sensitive)
if ($str1 === $str2) { echo "Identical"; } // False (case-sensitive)
```

### 2. **Comparison Operators**:
- `<`, `>`, `<=`, `>=`: Compare strings lexicographically.

```php
if ("apple" < "banana") { echo "True"; } // Outputs True
```

### 3. **`strcasecmp()`**:
- Case-insensitive string comparison.

```php
if (strcasecmp("Hello", "hello") == 0) { echo "Same"; } // True
```

