# Aprende un lenguaje de programación en un día (ejercicio voluntario para subir nota).

## Introducción

Cuando te sacaste el carnet de conducir, aprendiste las normas de circulación así como los fundamentos básicos para manejar un coche: volante, marchas, freno, acelerador, embrague, retrovisores... Seguramente, el coche que conduces ahora es diferente al que utilizaste para aprender a conducir, no obstante, lo puedes llevar sin problema. Cada coche tiene sus peculiaridades, pero quien sabe manejar un automóvil, puede adaptarse a las medidas, tacto y comportamiento de un vehículo en cuestión de horas.

Aprender a programar es como aprender a conducir. Si tienes una base sólida de programación y sabes manejar con soltura los tipos de datos, bucles, arrays, clases, métodos, etc. podrás pasar de un lenguaje a otro en un período relativamente corto, simplemente tendrás que adaptarte a la sintaxis y a las peculiaridades del nuevo lenguaje.

Con este ejercicio se pretende despertar el interés por otros lenguajes de programación distintos al que el alumno está estudiando como primer lenguaje.

Sigue los pasos que se indican a continuación.


## Miembros del grupo

* Rafael Campos Jurado
* Raul Moreno Montiel
* Germán Zambrana Ruiz

## Información sobre el lenguaje

Nuestro equipo ha seleccionado el lenguaje de programación C#.
C# (pronunciado si sharp en inglés) es un lenguaje de programación orientado a objetos desarrollado y estandarizado por Microsoft como parte de su plataforma .NET, que después fue aprobado como un estándar por la ECMA (ECMA-334) e ISO (ISO/IEC 23270). C# es uno de los lenguajes de programación diseñados para la infraestructura de lenguaje común.

Su sintaxis básica deriva de C/C++ y utiliza el modelo de objetos de la plataforma .NET, similar al de Java, aunque incluye mejoras derivadas de otros lenguajes.

## Herramientas de desarrollo

Para Windows y Linux  utilizaremos el IDE Visual Studio Code.
### Visual Studio Code
Microsoft Visual Studio es un entorno de desarrollo integrado (IDE, por sus siglas en inglés) para sistemas operativos Windows. Soporta múltiples lenguajes de programación, tales como C++, C#, Visual Basic .NET, F#, Java, Python, Ruby y PHP, al igual que entornos de desarrollo web, como ASP.NET MVC, Django, etc., a lo cual hay que sumarle las nuevas capacidades online bajo Windows Azure en forma del editor Monaco.


Visual Studio permite a los desarrolladores crear sitios y aplicaciones web, así como servicios web en cualquier entorno que soporte la plataforma .NET (a partir de la versión .NET 2002). Así, se pueden crear aplicaciones que se comuniquen entre estaciones de trabajo, páginas web, dispositivos móviles, dispositivos embebidos y consolas, entre otros.
<img src="/imagenes/visual.png" width="400px">

## Poniendo en práctica el lenguaje

Pon en práctica el lenguaje de programación realizando los siguientes ejercicios. Para cada uno de los ejercicios, pega el código fuente de la solución y una captura de pantalla.

### 1. ¡Hola mundo!

Realiza un programa que muestre por pantalla la frase **¡Hola mundo!**.
```C#
using System;

namespace HolaMundo
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("HOLA MUNDO!");
        }
    }
}
````
<img src ="/imagenes/HW1.jpg"  width = "700px">


### 2. Pirámide

Dada una altura introducida por el usuario, realiza un programa que pinte una pirámide a base de asteriscos con la altura indicada.
````C#
using System;

using System.Collections.Generic;
using System.Text;

namespace PiramideAsteriscos
{
    class Program
    {
        static void Main(string[] args)
        {
            
            Console.WriteLine("Programa que crea una pirámide de asteriscos");
            inicio:
            Console.WriteLine("inserta en número el nivel de la pirámide, mayor a cero");
            try
            {
                int nivel = int.Parse(Console.ReadLine());
                if (nivel != 0)
                {

                    int a;
                    int espacios;
                    for (int i = 1; i <= nivel; i++)
                    {
                        StringBuilder final = new StringBuilder();

                        espacios = nivel - i;
                        a = i + (i - 1);
                        for (int i1 = 0; i1 < espacios; i1++)
                            final.Append(" ");

                        for (int i2 = 0; i2 < a; i2++)
                            final.Append("*");

                        Console.WriteLine(final.ToString());

                    }
                }
                else
                {
                    System.Console.Clear();
                    goto inicio;
                }
               
            }
            catch (Exception )
            {
                System.Console.Clear();
                Console.WriteLine("El programa solo acepta números enteros");
                goto inicio;
               
            }

            
            Console.WriteLine("" + "\n" + "Aprieta una tecla para salir");
            Console.ReadLine();
        }
    }
}
````
<img src="/imagenes/piramide.jpg" width="700px">

### 3. Arrays y números aleatorios

Realiza un programa que rellene un array (o una estructura similar) con 20 números enteros aleatorios entre 1 y 100 y que seguidamente los muestre por pantalla. A continuación, se deben pasar los números primos a las primeras posiciones del array y los no primos a las posiciones restantes. Muestra finalmente el array resultado.

## Presentación de resultados

Cada equipo explicará al resto de la clase lo aprendido durante la realización del ejercicio. Todos los miembros de cada equipo deben participar en la explicación. Se puede utilizar como material de base para la presentación el repositorio de GitHub.

## Recompensa

* Todos los alumnos que realicen correctamente la actividad tendrán 0'25 puntos extra en la nota del trimestre.

* Los miembros del equipo más votado ganarán un premio.

:star: Si te ha gustado este ejercicio, dale una estrellita al [repositorio original](https://github.com/LuisJoseSanchez/aprende-un-lenguaje-en-un-dia).

