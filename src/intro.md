# Intro

Dies ist eine Sammlung an kurzen Beispielen (und "Lückentexten" ;-)) um ein bisschen
im Rahmen des Workshops mit Rust spielen zu können.

Auf den folgenden Seiten finden Sie jeweils eine Beschreibung und zumindest ein Codebeispiel.
Im Beispiel rechts oben finden Sie Buttons um den Code laufen zu lassen. Der Code kann
editiert werden. 
Die Beispiele enthalten Kommentare an Stellen die Aufgaben stellen, oder `todo!()`s wenn
eine Funktion fertiggestellt werden soll.

Sollte der Rust-Playground gerade down sein (leider öfter die letzten Tage), bitte [Rust Explorer](https://www.rustexplorer.com/b) verwenden.

Erinnerung: `println!("{:?}", ...)` und `dbg!(...)` können zum Ausgeben von vielen Typen verwendet werden.

Beispielslösungen sind darunter als solche gekennzeichnet und können mit dem "Auge"-Icon
sichtbar gemacht werden, z.B.:

```rust,editable
pub fn two_power_n(n: u32) -> u32 {
  todo!()
}
fn main() {
  assert_eq!(two_power_n(0), 1);
  assert_eq!(two_power_n(1), 2);
  assert_eq!(two_power_n(10), 1024);
}
```

```rust
// Beispielslösung
#pub fn two_power_n_loop(n: u32) -> u32 {
#  let mut result = 1;
#  for _ in 0..n {
#    result *= 2;
#  }
#  result
#}
#pub fn two_power_n_api(n: u32) -> u32 {
#  2_u32.pow(n)
#}
#
#fn main() {
#  assert_eq!(two_power_n_loop(0), 1);
#  assert_eq!(two_power_n_loop(1), 2);
#  assert_eq!(two_power_n_loop(10), 1024);
#
#  assert_eq!(two_power_n_api(0), 1);
#  assert_eq!(two_power_n_api(1), 2);
#  assert_eq!(two_power_n_api(10), 1024);
#}
```