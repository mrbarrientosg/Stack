# Stack

Tipo de dato abstracto implementado con una lista enlazada simple, en donde se pueden encontrar las principales funciones de una pila como lo seria **push**, **pop** y **top**. La implementación de la pila fue hecha con una lista enlazada simple.

## Instalación

#### OS X:

Deben tener instalado Xcode para poder compilar el archivo .xcodeproj

#### Windows y Linux:

Pueden usar cualquier IDE, y deben agregar los archivos Stack.h y Stack.c a su proyecto.

## Ejemplo

```C
#include <stdio.h>
#include <stdlib.h>
#include "Stack.h"

int main() {
    
    Stack * test = createStack(); // Se crea una nueva pila.
    
    /**
     Se puebla con valores de 0...9
     */
    int * data = NULL;
    
    int i;
    
    for (i = 0; i < 10; i++) {
        data = (int *)malloc(sizeof(int));
        *data = i;
        push(test, data);
    }
    
    while (emptyStack(test) == 0) {
        printf("%d\n", *(int *)top(test));
        free(pop(test));
    }
    
    // Se libera memoria del stack.
    free(test);
    
    return 0;
}

```
## Autor

* **Matias Barrientos** - [mrbarrientosg](https://github.com/mrbarrientosg)

## Licencia

Este proyecto esta bajo la licencia MIT - vea el archivo [LICENSE.md](LICENSE.md) para más detalles.
