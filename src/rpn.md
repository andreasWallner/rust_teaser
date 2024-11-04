# RPN Rechner

Die Rust Standardbibliothek hat - wie erwartet - auch implementierungen der
üblichen Standarddatentypen. Um uns ein bisschen mit diesen Vertraut zu machen
können wir uns [Vec](https://doc.rust-lang.org/std/vec/struct.Vec.html) ein bisschen genauer
anschaun, am Beispiel von einem RPN Rechner.

Die Berechnungsfunktion bekommt einen String übergeben und soll diesen element-für-element
verarbeiten. Elemente sind durch Leezeichen getrennt (eine Funktion zum splitten [existiert](https://doc.rust-lang.org/std/primitive.str.html#method.split_whitespace)).

Ein Vector kann als Stack verwendet werden (siehe Doku).

Zum parsen von Zahlen: Rust verwendet generell die `parse()` [Funktion](https://doc.rust-lang.org/std/primitive.str.html#method.parse) welche den Typen des Resultats aus der Verwendung ableitet.
Sie Dokumentation für Beispiele.

Zum Ausprobieren:
- Wie könnte die Funktion ohne die Library-Funktion zum splitten aussehen [Hinweis](https://doc.rust-lang.org/std/primitive.str.html#method.chars)
- Wie können wir bessere Fehlermeldungen zurückgeben (Hinweis: Der Fehlertyp kann auch ein enum sein)


```rust,editable
#[derive(Debug)]
struct SyntaxError;

fn rpn(input: &str) -> Result<f64, SyntaxError> {
    let mut stack = vec![0.0; 0];
    todo!()
}

fn main() {
    assert_eq!(dbg!(rpn("5 7 3 + /")).unwrap(), 0.5);
}
```

```rust
#[derive(Debug)]
#struct SyntaxError;
// Beispielslösung
#fn rpn(input: &str) -> Result<f64, SyntaxError> {
#    let mut stack = vec![0.0; 0];
#    for piece in input.split_whitespace() {
#        let parsed: Result<f64, _> = piece.parse();
#        match parsed {
#            Ok(number) => stack.push(number),
#            _ => {
#                let b = match stack.pop() {
#                    Some(num) => num,
#                    None => return Err(SyntaxError {})
#                };
#                let a = match stack.pop() {
#                    Some(num) => num,
#                    None => return Err(SyntaxError {})
#                };
#                let result = match piece {
#                    "+" => a+b,
#                    "-" => a-b,
#                    "*" => a*b,
#                    "/" => a/b,
#                    _ => return Err(SyntaxError),
#                };
#                stack.push(result);
#            }
#        }
#    }
#    if stack.len() != 1 {
#        return Err(SyntaxError);
#    }
#    Ok(stack[0])
#}
#
#fn main() {
#    assert_eq!(dbg!(rpn("5 7 3 + /")).unwrap(), 0.5);
#}
```