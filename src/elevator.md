# Lift Simulator

```rust
#[derive(Debug)]
enum Button {
  PressedUp,
  PressedDown,
  PressedBoth,
  Idle,
}
#[derive(Debug)]
enum Movement {
  Up,
  Down,
  Idle
}
#[derive(Debug)]
struct Elevator {
  pub current_floor: u8;
  pub movement: Movement;
  pub floors: Vec<Button>;
}

impl Elevator {
  pub fn new(floor_cnt: u8) -> Self {
    Self {
      current_floor: 0,
      floors: vec![Button::Idle; floor_cnt],
    }
  }
}
```