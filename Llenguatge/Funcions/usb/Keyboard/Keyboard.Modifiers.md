---
títol: Keyboard Modifiers and Special Keys
descripció: ""
categoria: "Funcions"
subcategoria: "Keyboard"
---




# Keyboard modifiers and special keys

## Descripció
Quan es dóna un caràcter ASCII imprimible com a argument, les funcions `Keyboard.write()`, `Keyboard.press()` i `Keyboard.release()` simulen accions sobre les tecles corresponents. Aquestes funcions també poden gestionar caràcters ASCII que requereixen prémer una tecla en combinació amb Maj o, en teclats internacionals, AltGr. Per exemple:

```
Keyboard.write('a');  // premeu i deixeu anar la tecla 'A'
Keyboard.write('A');  // premeu Shift i 'A', després deixeu anar totes dues.
```

Un teclat típic, però, té moltes tecles que no coincideixen amb un caràcter ASCII imprimible. Per simular aquestes, la biblioteca proporciona un conjunt de macros que es poden passar com a arguments a `Keyboard.write()`, `Keyboard.press()` i `Keyboard.release()`. Per exemple, la combinació de tecles Maj+F2 es pot generar amb:

```
Keyboard.press(KEY_LEFT_SHIFT);  // prem i mantén premut Shift
Keyboard.press(KEY_F2);          // prem i mantén premut F2
Keyboard.releaseAll();           // allibera ambdós
```

Tingueu en compte que, per a prémer múltiples tecles simultàniament, s'ha d'utilitzar link:../keyboardpress[`Keyboard.press()`] en lloc de link:../keyboardwrite[`Keyboard.write()`], ja que aquest últim només «polsa» les tecles (les prem i les deixa anar immediatament).
[%hardbreaks]

Les macros disponibles es llisten a continuació:

## Modificadors de teclat

Aquestes tecles estan destinades a modificar l'acció normal d'una altra tecla quan es premin les dues en combinació.

| Key | Hexadecimal | Decimal | Notes |
| --- | ----------- | ------- | ----- |
|KEY_LEFT_CTRL  |0x80 |128 |
|KEY_LEFT_SHIFT |0x81 |129 |
|KEY_LEFT_ALT   |0x82 |130 |Option (⌥) on Mac
|KEY_LEFT_GUI   |0x83 |131 |OS logo, Command (⌘) on Mac
|KEY_RIGHT_CTRL |0x84 |132 |
|KEY_RIGHT_SHIFT |0x85 |133 |
|KEY_RIGHT_ALT  |0x86 |134 |also AltGr, Option (⌥) on Mac
|KEY_RIGHT_GUI  |0x87 |135 |OS logo, Command (⌘) on Mac


## Tecles especials

Aquestes són totes les tecles que no coincideixen amb un caràcter ASCII imprimible i no són modificadores.


### Dins del bloc alfanumèric


|Key	|Hexadecimal 	|Decimal |
|---	|----------- 	|------- | 
|KEY_TAB        |0xB3 |179 |
|KEY_CAPS_LOCK  |0xC1 |193 |
|KEY_BACKSPACE  |0xB2 |178 |
|KEY_RETURN     |0xB0 |176 |
|KEY_MENU       |0xED |237 |



### Bloc de navegació


|Key	|Hexadecimal 	|Decimal |
|---	|----------- 	|------- |
|KEY_INSERT     |0xD1 |209 |
|KEY_DELETE     |0xD4 |212 |
|KEY_HOME       |0xD2 |210 |
|KEY_END        |0xD5 |213 |
|KEY_PAGE_UP    |0xD3 |211 |
|KEY_PAGE_DOWN  |0xD6 |214 |
|KEY_UP_ARROW   |0xDA |218 |
|KEY_DOWN_ARROW |0xD9 |217 |
|KEY_LEFT_ARROW |0xD8 |216 |
|KEY_RIGHT_ARROW |0xD7 |215 |



### Teclat numèric


|Key	|Hexadecimal 	|Decimal |
|---	|----------- 	|------- |
|KEY_NUM_LOCK   |0xDB |219 |
|KEY_KP_SLASH   |0xDC |220 |
|KEY_KP_ASTERISK |0xDD |221 |
|KEY_KP_MINUS   |0xDE |222 |
|KEY_KP_PLUS    |0xDF |223 |
|KEY_KP_ENTER   |0xE0 |224 |
|KEY_KP_1       |0xE1 |225 |
|KEY_KP_2       |0xE2 |226 |
|KEY_KP_3       |0xE3 |227 |
|KEY_KP_4       |0xE4 |228 |
|KEY_KP_5       |0xE5 |229 |
|KEY_KP_6       |0xE6 |230 |
|KEY_KP_7       |0xE7 |231 |
|KEY_KP_8       |0xE8 |232 |
|KEY_KP_9       |0xE9 |233 |
|KEY_KP_0       |0xEA |234 |
|KEY_KP_DOT     |0xEB |235 |


### Escapament i tecle de funció

La biblioteca pot simular les tecles de funció fins la F24


|Key	|Hexadecimal 	|Decimal |
|---	|----------- 	|------- |
|KEY_ESC        |0xB1 |177 |
|KEY_F1         |0xC2 |194 |
|KEY_F2         |0xC3 |195 |
|KEY_F3         |0xC4 |196 |
|KEY_F4         |0xC5 |197 |
|KEY_F5         |0xC6 |198 |
|KEY_F6         |0xC7 |199 |
|KEY_F7         |0xC8 |200 |
|KEY_F8         |0xC9 |201 |
|KEY_F9         |0xCA |202 |
|KEY_F10        |0xCB |203 |
|KEY_F11        |0xCC |204 |
|KEY_F12        |0xCD |205 |
|KEY_F13        |0xF0 |240 |
|KEY_F14        |0xF1 |241 |
|KEY_F15        |0xF2 |242 |
|KEY_F16        |0xF3 |243 |
|KEY_F17        |0xF4 |244 |
|KEY_F18        |0xF5 |245 |
|KEY_F19        |0xF6 |246 |
|KEY_F20        |0xF7 |247 |
|KEY_F21        |0xF8 |248 |
|KEY_F22        |0xF9 |249 |
|KEY_F23        |0xFA |250 |
|KEY_F24        |0xFB |251 |


### Teclat de funcions de control

Són les tres tecles que hi ha al damunt del bloc de navegació

|Key	|Hexadecimal 	|Decimal |
|---	|----------- 	|------- |
|KEY_PRINT_SCREEN |0xCE |206 |Print Screen or PrtSc / SysRq |
|KEY_SCROLL_LOCK  |0xCF |207 | |
|KEY_PAUSE        |0xD0 |208 |Pause / Break |



### Disposicions de teclats internacionals

Algunes disposicions nacionals defineixen claus addicionals. Per exemple, les disposicions sueca i danesa defineixen `KEY.A.RING` com a `0xB7`, que és la clau a la dreta de “P”, etiquetada com a “.” en aquestes disposicions i “{”/“[” en la disposició dels Estats Units. Per tal d'utilitzar aquestes definicions, s'ha d'incloure el fitxer correcte Keyboard_*.h. Per exemple:

```
#include <Keyboard.h>
#include <Keyboard_sv_SE.h> // extra key definitions from Swedish layout

void setup() {
  Keyboard.begin(KeyboardLayout_sv_SE); // use the Swedish layout
  Keyboard.write(KEY_A_RING);
}

void loop() {} // do-nothing loop
```

Per a la llista de definicions de tecles específiques de disposició, vegeu el fitxer respectiu de teclat*.h a les fonts de la biblioteca.


