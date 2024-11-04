# Collatz Sequenz

Die Collatz Sequenz ist definiert als:

- Wenn \\(n_i\\) 1 ist, endet die Serie
- Wenn \\(n_i\\) gerade ist, ist \\(n_{i+1} = n_i / 2\\)
- Wenn \\(n_i\\) ungerade ist, ist \\(n_{i+1} = 3 * n_i + 1\\)

(Ja, die Sequenz terminiert...)

Schreibe eine Funktion welche die Länge der Collatz-Sequenz für einen gegebenen Startwert ermittelt (Startwert und '1' inklusive).

Hinweis: ``while some_condition { ... }`` ist der syntax einer while Schleife, ``loop { ... }`` macht eine Endlosschleife. Siehe auch [Rust Book](https://doc.rust-lang.org/book/ch03-05-control-flow.html)

Zum Ausprobieren:
- sowohl eine Lösung mit Schleife oder eine mittels Rekursion sind möglich...

```rust,ignore
fn collatz_length(n: u32) -> usize {
  todo!()
}

fn main() {
  assert_eq!(collatz_length(3), 8);
  assert_eq!(collatz_length(1), 1);
}
```

```rust
#// Beispielslösung
#fn collatz_length(mut n: u32) -> usize {
#  let mut cnt = 1;
#  while n > 1 {
#    n = if n % 2 == 0 {
#      n / 2
#    } else {
#      3 * n + 1
#    };
#    cnt += 1;
#  }
#  cnt
#}
#fn main() {
#  assert_eq!(collatz_length(3), 8);
#  assert_eq!(collatz_length(1), 1);
#}
```