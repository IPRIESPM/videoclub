# Videoclub
En los siguientes ejercicios vamos a simular un pequeño proyecto de un Videoclub (basado en la propuesta que hace el tutorial de desarrolloweb.com), el cual vamos a realizar mediante un desarrollo incremental y siguiendo la práctica de programación en parejas (*pair programming*).

Antes de nada, crea un repositorio privado en GitHub y sube el proyecto actual de *Videoclub*. Una vez creado, invita a tu compañero al repositorio como colaborador.

- Inicializa en local tu repostorio de git, mediante `git init`
- Añade y sube los cambios a tu repositorio, mediante `git add .` y luego `git commit -m 'Inicializando proyecto'.`
- Conecta tu repositorio con GitHub y sube los cambios (mira la instrucciones de GitHub: comandos `git remote` y `git push`).
- Tu compañero deberá descargar el proyecto con sus credenciales.

**Proyecto no real**

El siguiente proyecto está pensado desde un punto de vista formativo. Algunas de las decisiones que se toman no se deben usar (como hacer `echo` dentro de las clases) o probar el código comparando el resultado en el navegador.

*Creamos el Soporte*

1. Crea una clase para almacenar soportes (`Soporte.php`). Esta clase será la clase padre de los diferentes soportes con los que trabaje nuestro videoclub (cintas de vídeo, videojuegos, etc...):
    - Crea el constructor que inicialice sus propiedades. Fíjate que la clase no tiene métodos *setters*.
    - Definir una constante mediante un propiedad privada y estática denominada `IVA con un valor del 21%
    - Crear un archivo (`inicio.php`) para usar las clases y copia el siguiente fragmento:
```php
<?php
include "Soporte.php";

$soporte1 = new Soporte("Tenet", 22, 3); 
echo "<strong>" . $soporte1->titulo . "</strong>"; 
echo "<br>Precio: " . $soporte1->getPrecio() . " euros"; 
echo "<br>Precio IVA incluido: " . $soporte1->getPrecioConIVA() . " euros";
$soporte1->muestraResumen();
```