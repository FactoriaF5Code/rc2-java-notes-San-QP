# Estructura de proyecto y tipos de archivo

Dentro de la carpeta `src` se guardan todos los archivos .java (CLASES). Estos se guardan en PACKAGES, que se COMPILAN (se traducen a 1s y 0s, en instrucciones nativas que pueden ser leídos por el ordenador) para poder ser leídos por la máquina.

Con la instalación de una versión de Java se incluye una máquina virtual que traduce lo que nosotros escribimos a un lenguaje intermedio, que después traduce a lenguaje-máquina puro. Este proceso hace que el código no cambie dependiendo del sistema operativo en el que trabajemos

## Nomenclaturas:
- La nomenclatura más normalizada de los PACKAGES es `com.nombreempresa`. Por ejemplo: *org.factoriaf5*
- Los JAVA CLASS (archivos .java) utilizan nomenclatura `CamelCase` con la primera en mayúscula.
- Palabras reservadas: `package`, `class`...

## Estructura de una clase .java:
Un archivo .java tiene en la primera linea el package al que pertenece. Por ejemplo: `package com.example`
~~~
package com.example

public class NombreClase{
    
    public static void main(String[]args){
        System.out.println("HolaMundo");

    }
}
~~~

- MÉTODO MAIN: `public static void main( String [ ] args ) { }`
Es el punto de entrada de la aplicación. Es necesario para ejecutar el código. **Este método no aplica en un entorno de desarrollo web.**
    - *public*: objeto público
    - *static*: objeto que pertenece a la clase NombreClase
    - *void*: tipo de retorno de una función que no devuelve nada, no hay return
    - *main*: nombre del método
    - *( String[ ]args )*: array de tipo String

## IMPRIMIR EN CONSOLA:
`System.out.println("HolaMundo"); = console.log() en js.`

El interior de los paréntesis siempre con comilla doble `""`

