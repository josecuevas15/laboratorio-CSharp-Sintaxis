# laboratorio-CSharp-Sintaxis
## 1 - Solicite el nombre de una persona, su edad y el nombre de una ciudad. 
Después de solicitar estos datos deberá mostrar por pantalla el siguiente mensaje:
Te llamas y tienes<años> años.Bienvenido a

### Solucion:
```csharp
Console.WriteLine("Introduzca su nombre:");
string nombre = Console.ReadLine();
Console.WriteLine("\nIntroduzca su edad:");
int edad = Convert.ToInt32(Console.ReadLine());
Console.WriteLine("\nIntroduzca el nombre de una ciudad:");
string ciudad = Console.ReadLine();
Console.WriteLine($"Te llamas {nombre}, tienes {edad} anios. Bienvenido a {ciudad}!");
```
## 2 – Solicite dos números y diga cual es el mayor.

### Solucion:
```csharp
Console.WriteLine("Introduzca un numero:");
int n1 = Convert.ToInt32(Console.ReadLine());

Console.WriteLine("\nIntroduzca otro numero:");
int n2 = Convert.ToInt32(Console.ReadLine());

if ( n1 > n2 )
{
    Console.WriteLine("El primero numero es mayor");
}
else if ( n2 > n1 )
{
    Console.WriteLine("El segundo numero es mayor.");
}
else
{
    Console.WriteLine("Los numeros son iguales!");
}
```
## 3 - Pedir el nombre de la semana al usuario y decirle si es fin de semana o no. En caso de error, indicarlo.

### Solucion:
```csharp
Console.WriteLine("Introduzca un dia de la semana:");
string dia = Console.ReadLine().ToLower();

switch ( dia ) {
    case "lunes":
    case "martes":
    case "miercoles":
    case "jueves":
    case "viernes":
        Console.WriteLine("No es fin de semana :(");
        break;
    case "sabado":
    case "domingo":
        Console.WriteLine("Es fin de semana! :D");
        break;
    default:
        Console.WriteLine("Eso no es un dia de la semana!");
        break;
}
```
## 4 - Recorre los números del 1 al 100. Muestra los números pares. Usar el tipo de bucle que quieras.

### Solucion:
```csharp
Console.WriteLine("NUMEROS PARES DEL 1 AL 100:");
for ( int i = 1; i <= 100; i++ )
{
    if (i % 2 == 0)
    {
        Console.WriteLine(i);
    }
}
```
## 5 – Solicitar un número al usuario y generar un Array con N números aleatorios. 
Por ejemplo, si el usuario introduce 4, el resultado por consola debería ser: 23, 34, 234, 11

### Solucion:
```csharp
Console.WriteLine("Introduzca la cantidad de numeros aleatorios que desea generar:");
int n = Convert.ToInt32(Console.ReadLine());

Random random = new Random();
int[] naleatorios = new int[n];

Console.WriteLine($"ELEMENTOS DEL ARRAY:{n}\n");
for ( int i = 0; i < n; i++ )
{
    int naleatorio = random.Next(0, 100);
    naleatorios[i] = naleatorio;
    Console.Write($"{naleatorio} ");
}
```
## 6 – Solicitar un número al usuario y un carácter. Crear una pirámide con N filas y el carácter solicitado
Por ejemplo, si el usuario introduce 5 y * el resultado por consola debería ser:

```
*
**
* *
*  *
*****
```

### Solucion:
```csharp
Console.WriteLine("Introduzca el numero de filas de la piramide.");
int filas = Convert.ToInt32(Console.ReadLine());

Console.WriteLine("Introduzca el caracter que va a componer la piramide:");
char caracter = Convert.ToChar(Console.ReadLine());

for (int i = 1; i < filas; i++)
{
    for(int j = 0; j <= i; j++)
    {
        if( i == (filas - 1))
        {
            Console.Write(caracter);
        }
        else
        {
            if (i == j)
            {
                Console.WriteLine(caracter);
            }
            else if (j == 0)
            {

                Console.Write(caracter);
            }
            else
            {

                Console.Write(" ");

            }
        }
    }
}
