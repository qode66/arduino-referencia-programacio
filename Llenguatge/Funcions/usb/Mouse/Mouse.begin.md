---
títol: "Mouse.begin"
descripció: ""
categoria: "Funcions"
subcategoria: "USB"
funcio: "Mouse"
---

# Mouse.begin()

### Descripció

Comença a emular el ratolí connectat a un ordinador. S'ha de cridar `Mouse.begin()` abans de controlar l'ordinador. Per finalitzar el control, utilitzeu `Mouse.end()`.

### Sintaxi

`Mouse.begin()`

### Paràmetres

Cap

### Devolucions

Res

### Exemple de codi

```
#include <Mouse.h>

void setup() {
  pinMode(2, INPUT);
}

void loop() {
  //initiate the Mouse library when button is pressed
  if (digitalRead(2) == HIGH) {
    Mouse.begin();
  }
}
```

### Vegeu també

* LLENGUATGE [Mouse](../Mouse.md)
* LLENGUATGE [Mouse.click()](./mouseClick.md)
* LLENGUATGE [Mouse.end()](./mouseEnd.md)
* LLENGUATGE [Mouse.move()](./mouseMove.md)
* LLENGUATGE [Mouse.press()](./mousePress.md)
* LLENGUATGE [Mouse.release()](./mouseRelease.md)
* LLENGUATGE [Mouse.isPressed()](./mouseIsPressed.md)

