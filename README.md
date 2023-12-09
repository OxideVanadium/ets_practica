<!-- Encabezados -->
# Title H1
## Title H2
### Title H3
#### Title H4
##### Title H5
###### Title H6

<!-- Linea -->
___
---

<!-- Listas desordenadas -->

* Manzana
    * Golden
    * Reinetas
* Pera
* Kiwi

<!-- Listas ordenadas -->
---
1. Primero
    1. Primero uno
    2. Primero dos
2. Segundo
3. Tercero
---
<!-- Tablas -->

| Nombre | Apellidos |
| -------|-----------|
| Juan | Perez |

<!-- Tipos de letra -->
---
Tipos de *letra* 

Tipos de **letra**

Letra ~~tachada~~

<!-- generar una linea de código -->
---
`
console.log("hola mundo")
`
```xml
<?xml version="1.0" encoding="UTF-8"?>
<?xml-stylesheet type="text/xsl" href="artistas.xsl"?>
<artistas>
<artista cod="a101">
<nombreCompleto>Diego Velázquez</nombreCompleto>
<nacimiento>1599</nacimiento>
<fallecimiento>1660</fallecimiento>
<pais>España</pais>
<fichaCompleta>https://es.wikipedia.org/wiki/Diego_Vel%C3%A1zquez</fichaCompleta>
</artista>
```
```python
def run(values: list) -> tuple:
    max_value = values[0]
    min_value = values[0]
    for value in values:
        if value < min_value:
            min_value = value
        elif value > max_value:
            max_value = value

    return max_value, min_value


if __name__ == '__main__':
    run([4, 6, 2, 1, 9, 63, -134, 566])
```
<!-- Accesso a páginas web -->
---
[Periodico El Pais](https://elpais.com/ "Periodico chachi")

[Google](https://www.google.com/)

<!-- Accesso a imagenes -->
![visual studio logo](https://1000logos.net/wp-content/uploads/2023/04/Visual-Studio-logo.png 'Logo Visual studio')
![Captura de pantalla](/42-67x45.png)

* [X] Tarea 1
* [X] Tarea 2
* [X] Tarea 3
* [ ] Tarea 4
