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

# Parte II: Método Nuevo de Entradas y C# Scripts para Movimientos del Personaje

## A continuación, se mostrará paso a paso cómo hacer que el personaje se mueva utilizando el nuevo método de entradas de Unity:

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

## Paso 6: Añade el componente _Player Input_ al objeto. En la sección de _Actions_, guarda este componente en la carpeta de tu elección. Al abrir el componente, verás varias jerarquías donde podrás ajustar los diferentes movimientos y acciones según el método de entrada (teclado, control, etc.).
![image](https://github.com/user-attachments/assets/3b2a25d4-d3e0-4ed4-bb4a-835fbec0618a)
![image](https://github.com/user-attachments/assets/af4db345-6682-4faa-9aea-4cb039137f0e)

## Paso 7: Inserta el script _PlayerMovement_ en el objeto. Este script controlará el movimiento del objeto dentro de la escena según las teclas asignadas en el paso anterior.
![image](https://github.com/user-attachments/assets/f0a0d748-86eb-49d0-bb4a-30a9805e77c5)
![image](https://github.com/user-attachments/assets/85fc7641-c984-4491-a0d9-3e68172f1c0e)

## Paso 8: Crea el prefab de la bala junto con sus scripts de movimiento y de autodestrucción. Además de añadirle un sphere collider y un rigidbody para que tuviera física.  
![Screenshot 2024-10-13 203835](https://github.com/user-attachments/assets/ffecc89d-8994-4cfa-96e1-af56a9784f4b)

## Paso 9: Añade el script _PlayerShooting_ al personaje/objeto. Este script controlará el disparo de la bala desde el personaje. A continuación, te mostramos el script que se encarga de disparar:
![image](https://github.com/user-attachments/assets/fb46d4e7-f15d-476e-aa06-34ea8b87b948)


## Al completar estos pasos, tu personaje debería poder moverse de manera rápida o lenta, rotar sobre el eje Y, disparar balas, y saltar. 
![Untitled video - Made with Clipchamp (4)](https://github.com/user-attachments/assets/e0911d30-4af0-4fae-b9cc-d2ed54f37bf8)
![Untitled video - Made with Clipchamp (5)](https://github.com/user-attachments/assets/5cf72540-5ce7-4ecd-bd28-68e8315b8db2)
![Untitled video - Made with Clipchamp (6)](https://github.com/user-attachments/assets/51a51e65-7625-4629-a547-125763e0e4bc)
![Untitled video - Made with Clipchamp (7)](https://github.com/user-attachments/assets/42eebe3d-93fb-4035-94b8-a535958be95c)


# Parte III: Algunos Detalles Adicionales
## Decidimos explorar un poco más y añadimos algunos componentes adicionales para mejorar el resultado final.
## Detalle #1: Seguimiento de la Cámara
## Para facilitar las grabaciones y mejorar la cinematografía, añadimos un script a la cámara principal para que siga al personaje mientras se desplaza por la escena. La cámara se ajusta utilizando dos variables: offset y smoothSpeed. Offset controla la distancia y el ángulo de la cámara respecto al personaje. smoothSpeed determina la suavidad del movimiento de la cámara al seguir al personaje.
![image](https://github.com/user-attachments/assets/953db868-e2b1-4cb1-8406-0cee0142f3f9)
![image](https://github.com/user-attachments/assets/dfcbd88b-57fc-48a8-9013-b4cbdd682a4e)

## Detalle #2: Tema Lunar
## Para este proyecto, decidimos mantener un tema lunar. Importamos desde la tienda un paisaje espacial llamado Lunar Landscape 3D, y luego insertamos el terreno proporcionado por el paquete. Finalmente, cambiamos el skybox a uno espacial (Milky Way). Para hacer este cambio, sigue estos pasos: Ve a Window > Rendering > Lighting > Environment. Haz drag and drop del cielo que deseas usar en el campo correspondiente.
![image](https://github.com/user-attachments/assets/2c11553b-a2ee-4461-a455-beab3772400a)
![image](https://github.com/user-attachments/assets/b52abd2c-32a3-4bd5-a54f-b3091e466b60)

# Opiniones Personales acerca del Proyecto

## Sebastián Negrón: 

## El proyecto me ayudó muchísimo a practicar la parte de la física y el movimiento en la creación de videojuegos. Durante las clases, me quedé con algunas lagunas y dificultades al entender ciertos conceptos, pero este reto me ayudó a solidificar mi conocimiento. Además, me gustó mucho explorar otros detalles adicionales, como el cambio del cielo y el terreno utilizado. Creo que encaja perfectamente con el diseño del robot.

## Mayra Lago:

## Este trabajo me sirvió para jugar un poco más con la física y las acciones dentro de un juego. Desde hacer que el robot tuviera "retroceso" a la hora de disparar o que las balas salieran saltando por el mapa. Por lo que me sirvió para explorar las mecánicas que se incorporaron y discutieron en clase. Aunque por otro lado, fue algo difícil lidiar con algunos problemas de sincronización en Unity, ya que en ocaciones las acciones que estaban programadas e implementadas no le funcionaban al resto de compañeros. Sin embargo pudimos realizar el trabajo de manera satisfactoria.  

## Jancarlos González:

## Este challenge me ayudo para entender el nuevo sistemas de input. Ya que el anterior a mi entender es mucho mas facil de entender como es que funciona, sin embargo el nuevo es mas facil de trabajar ya que no te tienes que saber mucho codigo para que funcione. Ademas de siempre con cada challenge repasar conceptos anteriores y descubrir cosas nuevas que no se habian dado en clase como en esta ocacion lo de la camara que es algo nuevo y que descubrio mi compañero Sebastian.

