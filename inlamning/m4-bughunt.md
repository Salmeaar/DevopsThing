## Let the bughunt begin

1.Jag lag till antäkningen "moi" sedan "wtf", varefter jag tog bort moi.

![Screenshot av staten efter bortagande av "moi"](./m4-Bilder/buggen-reproduced.png)


2.Code reviewn missa p.g.a charactär totalen testades inte efter deletering av antäckning

![Screeshot av terminalen då unit-testen failar](./m4-Bilder/test-fail.png)

Buggen fixades med att lägga till en rad i delete_item funktionen som tar
bort längden på antäckningen från totalen

![Screenshot på grön unit test](./m4-Bilder/grön-test.png)

4.För att ha undviki problemet från början borde man ha följt efter alla objekters väg till slutet