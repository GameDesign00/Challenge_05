# Go Ahead and Jump
# Introducción: 
## Este desafío busca profundizar en la física de los videojuegos. Pasaremos del método antiguo de entradas de Unity al nuevo Input System, que permite un control más flexible y robusto. A diferencia del método anterior, el nuevo sistema facilita la configuración de controles para múltiples plataformas, mejora la detección de entradas complejas y permite gestionar varios dispositivos al mismo tiempo (como teclado, mouse y gamepads) de manera más eficiente. Además, añadiremos dos movimientos: saltos y desplazamientos rápidos, simulando correr, para una experiencia de juego más dinámica y fluida.

# Parte I: Mapa de Entradas (Action Matrix)

## La siguiente tabla de acciones nos servirá de guía para motrar cómo decidimos configurar los inputs del jugador en el proyecto:

| Action                 | Mappings                                                |
|------------------------|---------------------------------------------------------|
| Horizontal movement     | A and D keys                                           |
| Vertical movement       | W and S keys, Up and Down arrows                       |
| Shoot                  | Mouse left click                                        |
| Jump                   | Spacebar                                                |
| Look                   | Mouse X movement                                        |
| Fast horizontal movement| Shift + A/D keys                                       |
| Fast vertical movement  | Shift + W/S keys                                       |

# Parte II: Metodo nuevo de entradas y C# scripts para movimientos del personaje
## A continuacion, mostraremos por pasos como hacer que el personaje se mueva utilizando el metodo nuevo de intradas de Unity:
## Paso 1: Dirigite en las opciones superiores del proyecto a Edit > Project Settings > Player > Active Input Handling y cambiaras la opcion a _Input Package System(New)_. El proyecto se reseteara y reresara con el nuevo sistema
## Paso 2: Dirigite a Window > Package Manager > Packages: Unity Registry > Input System. Instalaras este paquete para el proyecto (lo utilizaremos en el paso #6)
## Paso 3: Inserta el objeto que deseas aplicar el movimiento. Nosotros utilizamos el mismo robot de siempre del paquete de _SciFiWarriorPBRHPPolyart_.
## Paso 4: Anade el componente de _Capsule Collider_ al objeto. Centralizalo para que este parejo con el objeto.
## Paso 5: Anade el component de Rigidbody al objeto. Asegurate de activar la gravedad. Sugerimos que coloques debajo del objeto un plano o terreno para que este no se caiga al vacio infinito.
## Paso 6: Anade el componente _Player Input_ al objeto. En el componente, te dirigiras a la seccion de _Actions_. Te pedira que guardes este componente en la carpeta que usted prefiera dentro del proyecto. Una vez guardado, Abres el componente y veras varias jerarquias, donde puedes ajustar los diferentes movimientos basados en el metodo de input (tecldo, control...)
## Paso 7: Inserta los siguientes C# scripts al objeto: _PlayerMovement_. Este script se encargara de manejar que el objeto se desplaze a traves de la escena basado en las teclas que asignaste en el paso anterior.
## Paso 8: Crea el prefab de la bala:


# Parte III: Algunos detalles adiciionales
# Parte _: Opiniones Personales

## Sebastián Negrón:

## Mayra Lago:

## Jancarlos Gonzalez:

