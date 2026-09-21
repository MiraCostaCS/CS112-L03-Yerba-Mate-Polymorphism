## 📋 Project Assessment: Lab 03 - Mate + Polymorphism

### 1. Git & Workflow
- [ ] **Commit Messages:** Descriptive and incremental (e.g., "Implemented sip logic in CaffeinatedBeverage").

### 2. Functional Requirements
- [ ] **CaffeinatedBeverage (Base Class) upgraded to standards for model classes:**
    - [ ] **Encapsulation:** Private `name` (String), `ounces` (int), and `price` (double) with individual Getters/Setters.
    - [ ] **Validation:** Mutators and constructors ensure `ounces >= 0` and `price >= 0`.
    - [ ] **sip(int amount):** Correctly subtracts ounces; prevents negative values; returns `false` if 0 ounces remain, `true` otherwise.
    - [ ] **Standard Methods:** Full, default, and copy constructors; `setAll`; `toString`; and `equals` (using introspection/null checks).
- [ ] **Tea (Subclass):**
    - [ ] **Inheritance:** Correctly uses `extends CaffeinatedBeverage`.
    - [ ] **Instance Variables:** Private `brewTemp` (int) with validation in setter/constructor.
    - [ ] **toString():** Overridden with `@Override` to match: `Tea: name, ounces, brewed @ brewTemp°C, $price` (formatted as currency).
    - [ ] **equals():** Compares all fields including parent fields using `super.equals()` (which requires introspection in `CaffeinatedBeverage` to use `instanceof` operator.
- [ ] **YerbaMate (Subclass):**
    - [ ] **Inheritance:** Correctly uses `extends Tea`.
    - [ ] **Pass Logic:** `passMate()` method increments `numPasses` and prints the current count to the console.
    - [ ] **refill(int amount):** Correctly *adds* to (not resets) the inherited `ounces` variable.
    - [ ] **toString():** Overridden to match format: `Yerba Mate: name, ounces, brewTemp, price, numPasses passes so far`.
- [ ] **Driver Program (Main.java):**
    - [ ] **Polymorphism:** Uses a `CaffeinatedBeverage[]` array to store both `Tea` and `YerbaMate` objects.
    - [ ] **User Interface:** Menu-driven loop (1: Tea, 2: YerbaMate, 3: Exit) with appropriate scanner inputs added for new types.
    - [ ] **Array Processing:** On exit, prints all objects that are stored in `CaffeinatedBeverage` array.
      - [ ] **Priciest Yerba Mate:** Correctly identifies the highest-priced Yerba Mate using introspection and linear search algorithm.
      - [ ] **Average Price:** Correctly sums total price of each item in array, then calculates and prints the average price.

### 3. Code Quality & Standards
- [ ] **OOP Standards:**
    - [ ] Correct use of `super()` in constructors to initialize parent data.
    - [ ] Instance variables are strictly `private`.
- [ ] **Annotations:** `@Override` flag used correctly above all overridden methods.
- [ ] **Naming & Formatting:** `camelCase` for variables/methods; `PascalCase` for classes; consistent indentation and use of curly braces.
- [ ] **Constants:** Use of `final` constants for default data or shared values.
- [ ] **Documentation:** Every method (excluding `@Override`) and class includes JavaDoc syntax. Class-level descriptions and class-invariants are present.
