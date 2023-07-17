### Desafio: Calculadora de Média

Escreva um programa que solicite ao usuário que insira uma lista de números (separados por vírgula) e calcule a média dos números fornecidos. O programa deve exibir o resultado da média na tela.

Regras:

- Os números podem ser inteiros ou decimais.
- Os números podem ser positivos ou negativos.
- O programa deve lidar com uma lista de qualquer tamanho.


Exemplo de entrada 1:
```
Insira a lista de números: 5, 8, 12, 3, 6
````

Exemplo de saída 1:
```
A média é: 6.8
```

Exemplo de entrada 2:
```
Insira a lista de números: 10, -5, 2.5, 9, -3.5
```

Exemplo de saída 2:
```
A média é: 2.2
```

Você pode escolher a linguagem de programação que preferir e implementar a solução para este desafio. 

-----

### Respostas

#### Python

```python
def calcular_media():
    numeros = input("Insira a lista de números (separados por vírgula): ")
    lista = [float(num) for num in numeros.split(",")]

    soma = sum(lista)
    media = soma / len(lista)
    print("A média é:", round(media, 2))

calcular_media()

```

#### JavaScript

```javascript
function calcularMedia() {
  var numeros = prompt("Insira a lista de números (separados por vírgula):");
  var lista = numeros.split(",").map(Number);
  
  var soma = 0;
  for (var i = 0; i < lista.length; i++) {
    soma += lista[i];
  }
  
  var media = soma / lista.length;
  console.log("A média é: " + media.toFixed(2));
}

calcularMedia();
```


#### C#
```csharp
using System;

class Program
{
    static void Main()
    {
        CalcularMedia();
    }

    static void CalcularMedia()
    {
        Console.Write("Insira a lista de números (separados por vírgula): ");
        string numerosInput = Console.ReadLine();

        string[] numerosStr = numerosInput.Split(',');
        double[] numeros = new double[numerosStr.Length];

        for (int i = 0; i < numerosStr.Length; i++)
        {
            numeros[i] = Convert.ToDouble(numerosStr[i]);
        }

        double soma = 0;
        for (int i = 0; i < numeros.Length; i++)
        {
            soma += numeros[i];
        }

        double media = soma / numeros.Length;
        Console.WriteLine("A média é: " + media.ToString("F2"));
    }
}

```


#### Java
```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        calcularMedia();
    }

    public static void calcularMedia() {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Insira a lista de números (separados por vírgula): ");
        String numerosInput = scanner.nextLine();

        String[] numerosStr = numerosInput.split(",");
        double[] numeros = new double[numerosStr.length];

        for (int i = 0; i < numerosStr.length; i++) {
            numeros[i] = Double.parseDouble(numerosStr[i]);
        }

        double soma = 0;
        for (double numero : numeros) {
            soma += numero;
        }

        double media = soma / numeros.length;
        System.out.printf("A média é: %.2f\n", media);
        
        scanner.close();
    }
}

```



