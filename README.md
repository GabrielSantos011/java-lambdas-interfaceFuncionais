# java-lambdas-interfaceFuncionais
explicação para as principais interfaces funcionais

---

## Principais Interfaces Funcionais do Java

As principais **interfaces funcionais** do Java fazem parte do pacote `java.util.function`. Elas são fundamentais para programação funcional, permitindo expressões lambda e referências a métodos.

---

## 1. `Predicate<T>`

Representa uma função que testa uma condição e retorna um `boolean`.

- **Método principal:** `boolean test(T t)`

### Exemplo:
```java
Predicate<Integer> isEven = x -> x % 2 == 0;
System.out.println(isEven.test(4)); // true
```

---

## 2. `Function<T, R>`

Representa uma função que recebe um argumento e retorna um valor.

- **Método principal:** `R apply(T t)`

### Exemplo:
```java
Function<String, Integer> length = s -> s.length();
System.out.println(length.apply("Java")); // 4
```

---

## 3. `Consumer<T>`

Representa uma operação que recebe um argumento e não retorna nada.

- **Método principal:** `void accept(T t)`

### Exemplo:
```java
Consumer<String> print = s -> System.out.println(s);
print.accept("Hello, Java!"); // "Hello, Java!"
```

---

## 4. `Supplier<T>`

Representa uma função que não recebe argumentos e retorna um valor.

- **Método principal:** `T get()`

### Exemplo:
```java
Supplier<Double> random = () -> Math.random();
System.out.println(random.get()); // Exemplo: 0.6789123
```

---

## 5. `UnaryOperator<T>`

É uma especialização de `Function<T, T>` (entrada e saída do mesmo tipo).

- **Método principal:** `T apply(T t)`

### Exemplo:
```java
UnaryOperator<Integer> square = x -> x * x;
System.out.println(square.apply(5)); // 25
```

---

## 6. `BinaryOperator<T>`

Recebe dois argumentos do mesmo tipo e retorna um valor do mesmo tipo.

- **Método principal:** `T apply(T t1, T t2)`

### Exemplo:
```java
BinaryOperator<Integer> sum = (a, b) -> a + b;
System.out.println(sum.apply(3, 7)); // 10
```

---

Essas interfaces são amplamente utilizadas com a **Streams API**, **Collections** e facilitam a escrita de código mais limpo e funcional.
