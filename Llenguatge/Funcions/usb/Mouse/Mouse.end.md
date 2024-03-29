---
títol: "Mouse.end()"
descripció: ""
categoria: "Funcions"
subcategoria: "USB"
funcio: "Mouse"
---

# Mouse.end()

### Descripció

Deixa d'emular el ratolí connectat a un ordinador. Per iniciar el control, utilitzeu `Mouse.begin()`.

### Sintaxi

`Mouse.end()`

### Paràmetres

Cap

### Devolucions

Res

### Exemple de codi

```
#include <Mouse.h>

void setup() {
  pinMode(2, INPUT);
  //initiate the Mouse library
  Mouse.begin();
}

void loop() {
  //if the button is pressed, send a left mouse click
  //then end the Mouse emulation
  if (digitalRead(2) == HIGH) {
    Mouse.click();
    Mouse.end();
  }
}
```

### Vegeu també

* LLENGUATGE [Mouse](../Mouse.md)
* LLENGUATGE [Mouse.begin()](./mouseBegin.md)
* LLENGUATGE [Mouse.click()](./mouseClick.md)
* LLENGUATGE [Mouse.move()](./mouseMove.md)
* LLENGUATGE [Mouse.press()](./mousePress.md)
* LLENGUATGE [Mouse.release()](./mouseRelease.md)
* LLENGUATGE [Mouse.isPressed()](./mouseIsPressed.md)
