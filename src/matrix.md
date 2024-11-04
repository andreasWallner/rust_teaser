# Matrix Transpose

Arrays können - wie zu erwarten - auch arrays beinhalten.

``let array = [[1,2,3], [4,5,6], [7,8,9]];``

Wir können auch arrays erstellen mit die ein bestimmtes Element mehrmals beinhalten:

``let array = [[0; 3]; 3];``

Aufgabe: Schreibe eine Funktion die ein solches Array als Matrix interpretiert und transponiert. Die Funktion muss nur 3x3 Matrizen verarbeiten können.

Hinweis: ``for i in start..exclusive_end { ... }`` iteriert von ``start`` bis ``exclusive_end``.

Zum Ausprobieren:
- Was muss geändert werden um mit nur mit natürlichen Zahlen zu arbeiten?
- Was passiert bei Zugriffen ausserhalb des Arrays?


```rust,ignore
fn transpose(matrix: [[i32; 3]; 3]) -> [[i32; 3]; 3] {
  todo!()
}

fn main() {
  let input = [[1,2,3], [4,5,6], [7,8,9]];
  let transposed = transpose(input);
  assert_eq!(transposed, [[1,4,7],[2,5,8],[3,6,9]]);
}
```

```rust
/// Beispielslösung
#fn transpose(matrix: [[i32; 3]; 3]) -> [[i32; 3]; 3] {
#  let mut result = [[0; 3]; 3];
#  for i in 0..3 {
#    for j in 0..3 {
#      result[i][j] = matrix[j][i];
#    }
#  }
#  result
#}
#
#fn main() {
#  let input = [[1,2,3], [4,5,6], [7,8,9]];
#  let transposed = transpose(input);
#  assert_eq!(transposed, [[1,4,7],[2,5,8],[3,6,9]]);
#}
```