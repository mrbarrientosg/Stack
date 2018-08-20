# Stack

Tipo de dato abstracto para uso educativo o personal. Esta librería cuenta con todas las funciones principales de una pila como lo seria push, pop y top. La implementación de la pila fue hecha con una lista enlazad simple.

## Instalación

OS X:

Deben tener instalado Xcode para poder compilar el archivo .xcodeproj

Windows y Linux:

Pueden usar cualquier IDE, y deben agregar los archivos Stack.h y Stack.c a su proyecto.

## Ejemplo

```
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
## Contributing

Please read [CONTRIBUTING.md](https://gist.github.com/PurpleBooth/b24679402957c63ec426) for details on our code of conduct, and the process for submitting pull requests to us.

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/your/project/tags). 

## Authors

* **Billie Thompson** - *Initial work* - [PurpleBooth](https://github.com/PurpleBooth)

See also the list of [contributors](https://github.com/your/project/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* Hat tip to anyone whose code was used
* Inspiration
* etc
