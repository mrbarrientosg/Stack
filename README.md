# Stack

Tipo de dato abstracto implementado con una lista enlazada simple, en donde se pueden encontrar las principales funciones de una pila como lo seria **push**, **pop** y **top**. La implementación de la pila fue hecha con una lista enlazada simple.

## Instalación

#### OS X:

Deben tener instalado Xcode para poder compilar el archivo .xcodeproj

#### Windows y Linux:

Pueden usar cualquier IDE, y deben agregar los archivos stack.h y stack.c a su proyecto.

## Ejemplo

```C
#include <stdio.h>
#include <stdlib.h>
#include "stack.h"

int main() {
    
//    stack *test = stack_init (NULL);
    stack *test = stack_init (free); // Se crea una nueva pila.
    
    /**
     Se puebla con valores de 0...9
     */
    int * data = NULL;
    
    int i;
    
    for (i = 0; i < 10; i++) {
        data = (int *) malloc (sizeof (int));
        *data = i;
        stack_push (test, data);
    }
    
    while (stack_is_empty (test) == 0) {
        printf ("%d\n", *(int *) stack_top (test));
        stack_pop (test);
    }
    
    // Se libera memoria del stack.
    stack_release (&test);
    
    return 0;
}
```
## Autor

* **Matias Barrientos G** - [mrbarrientosg](https://github.com/mrbarrientosg)

## Licencia

Este proyecto esta bajo la licencia MIT - vea el archivo [LICENSE.md](LICENSE.md) para más detalles.
