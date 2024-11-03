# Fibonacci

Das altbekannte Programmierbeispiel, wir wollen die Fibonacchizahlen berechnen.

Als Erinnerung: die Sequenz beginnt mit `[0, 1]`, ab `n > 1` ist `fib(n) = fib(n-1) + fib(n-2)`

Zum Ausprobieren:
- Was passiert für große `n`?
- Wie können wir in solchen Fällen etwas "sinvolles" tun? (tipp [checked_add](https://doc.rust-lang.org/std/primitive.u8.html#method.checked_add))

Siehe auch: [Option Dokumentation](https://doc.rust-lang.org/std/option/)

```rust,editable
fn fib(n: u8) -> u8 {
  todo!()
}

fn main() {
  assert_eq!(fib(0), 0);
  assert_eq!(fib(1), 1);
  assert_eq!(fib(2), 1);
  assert_eq(fib(10), 55);
}
```

```rust
#fn fib(n: u8) -> u8 {
#  match n {
#    0 => 0,
#    1 => 1,
#    _ => fib(n-1) + fib(n-2)
#  }
#}
#
#fn fib_checked(n: u8) -> Option<u8> {
#  let result = match n {
#    x if x < 2 => x,
#    _ => {
#      let n_1 = fib_checked(n-1)?;
#      let n_2 = fib_checked(n-2)?;
#      n_1.checked_add(n_2)?
#    }
#  };
#  Some(result)
#}
#
#fn main() {
#  assert_eq!(fib(0), 0);
#  assert_eq!(fib(1), 1);
#  assert_eq!(fib(2), 1);
#  assert_eq!(fib(10), 55);
#  println!("{:?}", fib_checked(20));
#}
```