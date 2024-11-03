# Variablen

Normalerweise sind Variablen in Rust assign-once. Der selbe Name kann allerdings mehrmals verwendet werden.

Ist eine Variable mit `mut` deklariert, so kann diese verändert werden.

Zum Ausprobieren:

- müssen Typen angegeben werden?
- was passiert wenn die typen weggelassen werden?
- wie können Datentypen angegeben werden (bei deklaration, bei literals)

Siehe auch: [Rust Book](https://doc.rust-lang.org/book/ch03-01-variables-and-mutability.html)


```rust,editable
fn main() {
  let x = 5;
  assert_eq!(x, 5);

  // TODO überschreibe x mit 3.14
  // let...
  assert_eq!(x, 3.14);

  // TODO erstelle eine mutierbare Variable `sum`
  for i in 0..10 {
    // TODO summiere alle i auf, das print gibt die zwischenwerte aus
    println!("{}", sum)
  }
  assert_eq!(sum, 45);
}
```

```rust
// Beispielslösung
#fn main() {
#  let x = 5;
#  assert_eq!(x, 5);
#
#  let x = 3.14;
#  assert_eq!(x, 3.14);
#
#  let mut sum = 0;
#  for i in 0..10 {
#    sum += i;
#    println!("{}", sum)
#  }
#  assert_eq!(sum, 45);
#}
```