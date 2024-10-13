# Go Ahead and Jum

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

# Parte II: Método Nuevo de Entradas y C# Scripts para Movimientos del Personaje

## A continuación, te mostraremos paso a paso cómo hacer que el personaje se mueva utilizando el nuevo método de entradas de Unity:

## Paso 1: Ve a Edit > Project Settings > Player > Active Input Handling y cambia la opción a Input Package System (New). El proyecto se reiniciará y volverá con el nuevo sistema de entradas activado.
![image](https://github.com/user-attachments/assets/f3f77d46-59d2-4325-9a6f-719a29eb31e2)

## Paso 2: Dirígete a Window > Package Manager > Packages: Unity Registry > Input System. Instala este paquete para el proyecto, lo cual será necesario en el paso #6.
![image](https://github.com/user-attachments/assets/f94d75aa-ea17-4f83-a338-075accc8f423)

## Paso 3: Inserta el objeto que deseas mover. En este ejemplo, utilizamos el robot del paquete _SciFiWarriorPBRHPPolyart_.
![image](https://github.com/user-attachments/assets/0fef219f-f757-4cf9-87a7-cf976f5645a1)

## Paso 4: Añade el componente _Capsule Collider_ al objeto. Asegúrate de centralizarlo para que quede alineado con el objeto.
![image](https://github.com/user-attachments/assets/fcf2da81-2b96-43e0-86ae-d647846131c3)

## Paso 5: Añade el componente _Rigidbody_ al objeto y activa la gravedad. Te sugerimos colocar un plano o terreno debajo del objeto para evitar que caiga al vacío.
![image](https://github.com/user-attachments/assets/4677b060-eb9a-49ae-b2a4-de288dd89ee9)

## Paso 6: Añade el componente _Player Input_ al objeto. En la sección de Actions, guarda este componente en la carpeta de tu elección. Al abrir el componente, verás varias jerarquías donde podrás ajustar los diferentes movimientos y acciones según el método de entrada (teclado, control, etc.).
## Paso 7: Inserta el script _PlayerMovement_ en el objeto. Este script controlará el movimiento del objeto dentro de la escena según las teclas asignadas en el paso anterior.
## Paso 8: Crea el prefab de la bala junto con su script. para hacer esto tienes que... (PON INFORMACION AQUI NO ME RECUERDO BIEN EL PROCESO 😔)
## Paso 9: Añade el script _PlayerShooting_ al personaje/objeto. Este script controlará el disparo de la bala desde el personaje. A continuación, te mostramos el script que se encarga de disparar:
## Al completar estos pasos, tu personaje debería poder moverse de manera rápida y lenta, rotar sobre el eje Y, disparar balas, y saltar.

# Parte III: Algunos detalles adiciionales

# Opiniones Personales acerca del Proyecto

## Sebastián Negrón:

## Mayra Lago:

## Jancarlos Gonzalez:

